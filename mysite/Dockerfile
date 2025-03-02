# ベースイメージ
FROM python:3.10

# ワーキングディレクトリを作成
WORKDIR /code

# 必要なファイルをコピー
COPY requirements.txt /code/
COPY . /code/

# pip を最新化
RUN pip install --upgrade pip setuptools wheel

# 依存関係をインストール
RUN pip install -r requirements.txt

# 8000 番ポートを開放
EXPOSE 8000

# CMD を JSON 形式で指定（Docker の警告を防ぐ）
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
