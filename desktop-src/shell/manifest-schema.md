---
description: Estos elementos son el esquema XML usado en el manifiesto de transferencia de los asistentes para publicación web y ordenación de impresión en línea.
title: Esquema de manifiesto de transferencia
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d0b57f1eb81169674c6c8d36e66c8a3cd21cf0e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572505"
---
# <a name="transfer-manifest-schema"></a>Esquema de manifiesto de transferencia

Estos elementos son el esquema XML usado en el manifiesto de transferencia de los asistentes para publicación web y ordenación de impresión en línea.

Los siguientes elementos se definen para el manifiesto de transferencia.

-   [cancelledpage](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [failurepage](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [Favorito](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [file](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [Filelist](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [Carpeta](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [folderlist](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [formdata](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [htmlui](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [imageproperty](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [metadata](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [netplace](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [Exponer](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [Redimensionar](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [successpage](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [Destino](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [transfermanifest](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [uploadinfo](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)

## <a name="cancelledpage"></a>cancelledpage

Especifica la página HTML del lado servidor que se mostrará antes de cerrar el asistente cuando el usuario haga clic en **el botón** Cancelar.

### <a name="syntax"></a>Sintaxis


```
<cancelledpage
    href = "string"
>
<!-- child elements -->
</cancelledpage>                  
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                                           |
|-----------|-------------------------------------------------------------------------------------------------------|
| href      | Necesario. Dirección URL de la página HTML del lado servidor que se mostrará cuando el usuario haga clic en **el botón** Cancelar. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios |
|-----------------------|----------------|
| [uploadinfo](#syntax) | None           |



 

## <a name="failurepage"></a>failurepage

Especifica la página HTML del lado servidor que se mostrará si la carga no se realiza correctamente.

### <a name="syntax"></a>Sintaxis


```
<failurepage
    href = "string"
>
<!-- child elements -->
</failurepage>                    
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                                |
|-----------|--------------------------------------------------------------------------------------------|
| href      | Necesario. Dirección URL de la página HTML del lado servidor que se va a mostrar si la carga no se realiza correctamente. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Ninguno. Se permite el texto. |



 

## <a name="favorite"></a>Favorito

Indica al asistente que cree una entrada de sitio web favorita en el **menú Favoritos** de la dirección URL especificada. Si no se especifica este elemento, el [elemento htmlui](#syntax) se usa en su lugar.

### <a name="syntax"></a>Sintaxis


```
<favorite
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</favorite>                   
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descripción                                                            |
|-----------|------------------------------------------------------------------------|
| comment   | Necesario. Comentario asociado a la **entrada Favoritos.**         |
| href      | Necesario. Dirección URL de la **entrada Favoritos.**                          |
| name      | Necesario. Nombre de la dirección URL que aparece en **el menú Favoritos.** |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Ninguno. Se permite el texto. |



 

## <a name="file"></a>archivo

Describe un único archivo que se va a copiar. Varios [elementos](#syntax) de archivo pueden estar contenidos en un único [nodo de lista de](#syntax) archivos.

### <a name="syntax"></a>Sintaxis


```
<file
    contenttype = "string"
    destination = "string"
    extension = "string"
    id = "string"
    size = "string"
    source = "string"
>
<!-- child elements -->
</file>                   
                    
```



### <a name="attributes"></a>Atributos



| Atributo   | Descripción                                                                                                                                                                  |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Contenttype | Opcional. Tipo MIME del archivo.                                                                                                                                         |
| destination | Necesario. Ruta de acceso sugerida para el archivo una vez cargado. Esta ruta de acceso es relativa a la dirección URL de destino del sitio de carga. El sitio de carga puede modificar este valor según sea necesario. |
| extensión   | Opcional. Extensión de nombre de archivo del archivo.                                                                                                                               |
| id          | Necesario. Índice numérico del archivo.                                                                                                                                   |
| tamaño        | Opcional. Tamaño del archivo, en bytes.                                                                                                                                    |
| source      | Necesario. Ruta de acceso completa del sistema de archivos para el archivo.                                                                                                                            |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario      | Elementos secundarios                                          |
|---------------------|---------------------------------------------------------|
| [Filelist](#syntax) | [metadata](#syntax), [post ,](#syntax) [resize](#syntax) |



 

## <a name="filelist"></a>Filelist

Contenedor para los elementos que describen los archivos que se van a copiar. Varios [elementos filelist](#syntax) pueden estar contenidos en un único [nodo transfermanifest.](#syntax)

### <a name="syntax"></a>Sintaxis


```
<filelist
    usesfolders = "1"
>
<!-- child elements -->
</filelist>                   
                    
```



### <a name="attributes"></a>Atributos



| Atributo   | Descripción      |
|-------------|------------------|
| usesfolders | Sin implementar. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario              | Elementos secundarios  |
|-----------------------------|-----------------|
| [transfermanifest](#syntax) | [file](#syntax) |



 

## <a name="folder"></a>folder

Describe una carpeta en la que se almacenan los archivos. Varios [elementos de](#syntax) carpeta pueden estar contenidos en un único nodo de lista [de](#syntax) carpetas.

### <a name="syntax"></a>Sintaxis


```
<folder
    destination = "string"
>
<!-- child elements -->
</folder>                 
                    
```



### <a name="attributes"></a>Atributos



| Atributo   | Descripción                                                                                                                                                                    |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| destination | Necesario. Ruta de acceso sugerida para la carpeta una vez cargada. Esta ruta de acceso es relativa a la dirección URL de destino del sitio de carga. El sitio de carga puede modificar este valor según sea necesario. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios |
|-----------------------|----------------|
| [folderlist](#syntax) | None           |



 

## <a name="folderlist"></a>folderlist

Contenedor para los elementos que describen los archivos que se van a copiar. Varios [elementos folderlist](#syntax) pueden estar contenidos en un único [nodo transfermanifest.](#syntax)

### <a name="syntax"></a>Sintaxis


```
<folderlist>
<!-- child elements -->
</folderlist>                 
                    
```



### <a name="attributes"></a>Atributos

Ninguno.

### <a name="element-information"></a>Información de elemento



| Elemento primario              | Elementos secundarios    |
|-----------------------------|-------------------|
| [transfermanifest](#syntax) | [Carpeta](#syntax) |



 

## <a name="formdata"></a>formdata

Describe los datos opcionales de formulario codificados en HTML que se pueden transferir con los archivos. El servicio agrega este elemento si elige cargar los archivos como una publicación de varias partes. Los datos del formulario, junto con la información del [elemento post,](#syntax) se usan para crear el encabezado de publicación.

Varios [elementos formdata](#syntax) pueden estar contenidos en un único [nodo uploadinfo.](#syntax)

### <a name="syntax"></a>Sintaxis


```
<formdata
    name = "string"
>
<!-- child elements -->
</formdata>                   
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                      |
|-----------|----------------------------------------------------------------------------------|
| name      | Necesario. Define el nombre de datos del formulario asociado a esta sección de la carga. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios |
|-----------------------|----------------|
| [uploadinfo](#syntax) | None           |



 

## <a name="htmlui"></a>htmlui

Dirección URL de la página HTML del lado servidor que se va a mostrar cuando se cierre el asistente. Este elemento crea una entrada de página [](#syntax) web favorita en el menú **Favoritos** si el elemento favorito no está presente y se especifica el nombre descriptivo del sitio de carga.

### <a name="syntax"></a>Sintaxis


```
<htmlui
    href = "string"
>
<!-- child elements -->
</htmlui>                 
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                          |
|-----------|--------------------------------------------------------------------------------------|
| href      | Necesario. Dirección URL de la página HTML del lado servidor que se va a mostrar cuando se cierre el asistente. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Ninguno. Se permite texto. |



 

## <a name="imageproperty"></a>imageproperty

Especifica una propiedad de imagen relacionada con el archivo. Varios [elementos imageproperty](#syntax) pueden estar contenidos en un único nodo [de metadatos.](#syntax)

### <a name="syntax"></a>Sintaxis


```
<imageproperty
    id = "string"
>
<!-- child elements -->
</imageproperty>                  
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descripción                                  |
|-----------|----------------------------------------------|
| id        | Necesario. Identificador de la propiedad determinada. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario      | Elementos secundarios         |
|---------------------|------------------------|
| [metadata](#syntax) | Ninguno. Se permite texto. |



 

## <a name="metadata"></a>metadata

Contenedor para elementos y texto que define metadatos para el archivo determinado. Varios [elementos de](#syntax) metadatos pueden estar contenidos en un único nodo [de](#syntax) archivo.

### <a name="syntax"></a>Sintaxis


```
<metadata>
<!-- child elements -->
</metadata>                   
                    
```



### <a name="attributes"></a>Atributos

Ninguno.

### <a name="element-information"></a>Información de elemento



| Elemento primario  | Elementos secundarios           |
|-----------------|--------------------------|
| [file](#syntax) | [imageproperty](#syntax) |



 

## <a name="netplace"></a>netplace

Define el destino de un lugar de red que se crea en **Mis lugares de red** cuando se completa la carga. La creación de un lugar de red se puede evitar mediante el [**método IPublishingWizard::Initialize.**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize)

### <a name="syntax"></a>Sintaxis


```
<netplace
    comment = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</netplace>                   
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                                     |
|-----------|-------------------------------------------------------------------------------------------------|
| comment   | Necesario. Comentario que se muestra para el icono de posición de red cuando el cursor se encuentra sobre él.         |
| href      | Necesario. Dirección URL de la entrada de la posición de red.                                                   |
| name      | Necesario. El nombre del icono de lugar de red que aparece en la **carpeta Mis lugares de** red. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Ninguno. Se permite texto. |



 

## <a name="post"></a>post

Dirección URL en la que se debe publicar el archivo. El servicio agrega este elemento cuando la transferencia se realiza como una publicación de varias partes y, con [formdata,](#syntax)se usa para compilar el encabezado de publicación. Si el servicio elige realizar la transferencia de archivos mediante World Wide Web Distributed Authoring and Versioning (WebDAV), no debe agregar este elemento. Varios [elementos post](#syntax) pueden estar contenidos en un único nodo [de](#syntax) archivo.

### <a name="syntax"></a>Sintaxis


```
<post
    filename = "string"
    href = "string"
    name = "string"
>
<!-- child elements -->
</post>                   
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                    |
|-----------|--------------------------------------------------------------------------------|
| nombreDeArchivo  | Opcional. Nombre de archivo del archivo publicado.                                   |
| href      | Necesario. Dirección URL de la carpeta de destino.                                   |
| name      | Necesario. Define el nombre de datos del formulario asociado a esta sección de la publicación. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario  | Elementos secundarios      |
|-----------------|---------------------|
| [file](#syntax) | [formdata](#syntax) |



 

## <a name="resize"></a>resize

Define el escalado y la recompresión de un archivo de imagen en formato JPEG. Si el archivo de origen ya está en formato JPEG y es menor o igual que el ancho y alto especificados, no tiene tamaño. Si el archivo de origen no es un archivo JPEG, se convierte. El escalado, la recompresión y la conversión del archivo se pueden evitar mediante el [**método IPublishingWizard::Initialize.**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) Varios [elementos de](#syntax) cambio de tamaño pueden estar contenidos en un único nodo [de](#syntax) archivo.

### <a name="syntax"></a>Sintaxis


```
<resize
    cx = "string"
    cy = "string"
    quality = "string"
>
<!-- child elements -->
</resize>                 
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                                                                                                         |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cx        | Necesario. Ancho de la imagen, en píxeles, después de la carga. Si este valor es 0, **cx** se calcula a partir del valor **cy** para conservar las dimensiones relativas.  |
| cy        | Necesario. Alto de la imagen, en píxeles, después de la carga. Si este valor es 0, **cy** se calcula a partir del valor **cx** para conservar las dimensiones relativas. |
| calidad   | Necesario. El valor de calidad JPEG, entre 0 y 100, siendo 100 la calidad más alta.                                                                            |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario  | Elementos secundarios |
|-----------------|----------------|
| [file](#syntax) | Ninguno.          |



 

## <a name="successpage"></a>successpage

Especifica la página HTML del lado servidor que se mostrará si la carga se realiza correctamente.

### <a name="syntax"></a>Sintaxis


```
<successpage
    href = "string"
>
<!-- child elements -->
</successpage>                    
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                            |
|-----------|----------------------------------------------------------------------------------------|
| href      | Necesario. Dirección URL de la página HTML del lado servidor que se va a mostrar si la carga se realiza correctamente. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Ninguno. Se permite texto. |



 

## <a name="target"></a>Destino

Carpeta de destino especificada en formato UNC (Convención de nomenclatura universal) o como servidor WebDAV. El servicio agrega este destino para especificar una carpeta de destino si la transferencia usa un protocolo webDAV o del sistema de archivos. Si el servicio elige realizar la transferencia de archivos como una publicación de varias partes, no debe agregar este elemento.

### <a name="syntax"></a>Sintaxis


```
<target
    href = "string"
>
<!-- child elements -->
</target>                 
                    
```



### <a name="attributes"></a>Atributos



| Atributo | Descripción                                                                                                                 |
|-----------|-----------------------------------------------------------------------------------------------------------------------------|
| href      | Necesario. Dirección URL de la carpeta de destino. Use el **https://** para WebDAV o el formulario de recurso **\\ \\ \\ compartido de** servidor para UNC. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Ninguno. Se permite texto. |



 

## <a name="transfermanifest"></a>transfermanifest

Nodo primario del archivo de manifiesto de transferencia.

### <a name="syntax"></a>Sintaxis


```
<transfermanifest>
<!-- child elements -->
</transfermanifest>                   
                    
```



### <a name="attributes"></a>Atributos

Ninguno.

### <a name="element-information"></a>Información de elemento



| Elemento primario | Elementos secundarios                                                    |
|----------------|-------------------------------------------------------------------|
| Ninguno           | [filelist](#syntax), [folderlist](#syntax), [uploadinfo](#syntax) |



 

## <a name="uploadinfo"></a>uploadinfo

Contenedor para los elementos que proporcionan información del sitio de carga utilizado en la transacción. Varios [elementos uploadinfo](#syntax) pueden estar contenidos en un único [nodo transfermanifest.](#syntax)

### <a name="syntax"></a>Sintaxis


```
<uploadinfo
    friendlyname = "string"
>
<!-- child elements -->
</uploadinfo>                 
                    
```



### <a name="attributes"></a>Atributos



| Atributo    | Descripción                                                                 |
|--------------|-----------------------------------------------------------------------------|
| friendlyname | Necesario. Nombre descriptivo del sitio web que se muestra en el asistente. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario              | Elementos secundarios                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [transfermanifest](#syntax) | [cancelledpage](#syntax), [failurepage](#syntax), [favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax) |



 

 

 



