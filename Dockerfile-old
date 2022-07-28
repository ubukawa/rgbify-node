FROM osgeo/gdal:ubuntu-small-3.4.0
RUN apt update \
&& apt upgrade -y \
&& apt install -y sudo\
&& curl -sL https://deb.nodesource.com/setup_16.x | bash - \
&& apt update \

&& apt install -y \
autoconf \
automake \
g++ \
nodejs \
zip \
gdal-bin \
git \
libgdal-dev \
libproj-dev \
python3-numpy \
python3-pip \
python3-rasterio \
rasterio \
sqlite3 \
&& git clone https://github.com/mapbox/rio-rgbify.git \
&& cd rio-rgbify \
&& pip install -e '.[test]' \
&& cd .. \
&& git clone https://github.com/mapbox/mbutil \
&& cd mbutil \
&& python setup.py install \
&& cd .. \
&& git clone https://github.com/mapbox/tippecanoe \
&& cd tippecanoe \
&& make -j3 LDFLAGS="-latomic" \
&& make install \
&& cd .. \