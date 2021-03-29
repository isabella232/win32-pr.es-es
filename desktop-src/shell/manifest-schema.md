---
description: Estos elementos componen el esquema XML que se usa en el manifiesto de transferencia del Asistente para la publicación web y el orden de impresión en línea.
title: Transferir esquema de manifiesto
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 488b6fc9-ff85-4860-9cd5-61d5de7e15e8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: d0b57f1eb81169674c6c8d36e66c8a3cd21cf0e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104997837"
---
# <a name="transfer-manifest-schema"></a>Transferir esquema de manifiesto

Estos elementos componen el esquema XML que se usa en el manifiesto de transferencia del Asistente para la publicación web y el orden de impresión en línea.

Los siguientes elementos se definen para el manifiesto de transferencia.

-   [cancelledpage](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [failurepage](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [Favoritos](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [file](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [FileList](#syntax)
    -   [Sintaxis](#syntax)
    -   [Atributos](#attributes)
    -   [Información de elemento](#element-information)
-   [directorio](#syntax)
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
-   [cambiar el tamaño](#syntax)
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

Especifica la página HTML del lado servidor que se va a mostrar antes de que el asistente se cierre cuando el usuario haga clic en el botón **Cancelar** .

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
| href      | Obligatorio. Dirección URL de la página HTML del lado servidor que se va a mostrar cuando el usuario haga clic en el botón **Cancelar** . |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios |
|-----------------------|----------------|
| [uploadinfo](#syntax) | Ninguno           |



 

## <a name="failurepage"></a>failurepage

Especifica la página HTML del lado servidor que se va a mostrar si la carga no se realiza correctamente.

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
| href      | Obligatorio. Dirección URL de la página HTML del servidor que se va a mostrar si la carga no se realiza correctamente. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Ninguno. Se permite el texto. |



 

## <a name="favorite"></a>Favoritos

Indica al asistente que cree una entrada de sitio web favorita en el menú **Favoritos** de la dirección URL especificada. Si no se especifica este elemento, el elemento [htmlui](#syntax) se usa en su lugar.

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
| comment   | Obligatorio. Comentario asociado a la entrada **Favoritos** .         |
| href      | Obligatorio. Dirección URL de la entrada de **Favoritos** .                          |
| name      | Necesario. El nombre de la dirección URL que aparece en el menú **Favoritos** . |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Ninguno. Se permite el texto. |



 

## <a name="file"></a>archivo

Describe un solo archivo que se va a copiar. Se pueden incluir varios elementos de [archivo](#syntax) en un solo nodo [FileList](#syntax) .

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
| ContentType | Opcional. Tipo MIME del archivo.                                                                                                                                         |
| destination | Obligatorio. Una ruta de acceso sugerida para el archivo una vez cargado. Esta ruta de acceso es relativa a la dirección URL de destino del sitio de carga. El sitio de carga puede modificar este valor según sea necesario. |
| extensión   | Opcional. La extensión de nombre de archivo del archivo.                                                                                                                               |
| id          | Obligatorio. Índice numérico del archivo.                                                                                                                                   |
| tamaño        | Opcional. Tamaño del archivo, en bytes.                                                                                                                                    |
| source      | Obligatorio. Ruta de acceso completa del sistema de archivos para el archivo.                                                                                                                            |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario      | Elementos secundarios                                          |
|---------------------|---------------------------------------------------------|
| [FileList](#syntax) | [metadatos](#syntax), [post](#syntax), [cambiar tamaño](#syntax) |



 

## <a name="filelist"></a>FileList

Contenedor de elementos que describen los archivos que se van a copiar. Varios elementos [FileList](#syntax) pueden estar contenidos en un único nodo [transfermanifest](#syntax) .

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

Describe una carpeta en la que se almacenan los archivos. Varios elementos de [carpeta](#syntax) pueden estar contenidos en un único nodo de [folderList](#syntax) .

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
| destination | Obligatorio. Una ruta de acceso sugerida para la carpeta una vez cargada. Esta ruta de acceso es relativa a la dirección URL de destino del sitio de carga. El sitio de carga puede modificar este valor según sea necesario. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios |
|-----------------------|----------------|
| [folderlist](#syntax) | Ninguno           |



 

## <a name="folderlist"></a>folderlist

Contenedor de elementos que describen los archivos que se van a copiar. Varios elementos [folderList](#syntax) pueden estar contenidos en un único nodo [transfermanifest](#syntax) .

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
| [transfermanifest](#syntax) | [directorio](#syntax) |



 

## <a name="formdata"></a>formdata

Describe datos de formulario codificados en HTML opcionales que se pueden transferir con los archivos. El servicio agrega este elemento si opta por cargar los archivos como una publicación de varias partes. Los datos del formulario, junto con información del elemento [post](#syntax) , se usan para crear el encabezado post.

Varios elementos [formData](#syntax) pueden estar contenidos en un único nodo [uploadinfo](#syntax) .

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
| [uploadinfo](#syntax) | Ninguno           |



 

## <a name="htmlui"></a>htmlui

Dirección URL de la página HTML del servidor que se va a mostrar cuando se cierre el asistente. Este elemento crea una entrada de página web favorita en el menú **Favoritos** si el elemento [favorito](#syntax) está ausente y se especifica el nombre descriptivo del sitio de carga.

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
| href      | Obligatorio. Dirección URL de la página HTML del servidor que se va a mostrar cuando se cierre el asistente. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Ninguno. Se permite el texto. |



 

## <a name="imageproperty"></a>imageproperty

Especifica una propiedad de imagen relacionada con el archivo. Varios elementos [imageproperty](#syntax) pueden estar contenidos en un solo nodo de [metadatos](#syntax) .

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
| id        | Obligatorio. IDENTIFICADOR de la propiedad determinada. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario      | Elementos secundarios         |
|---------------------|------------------------|
| [metadata](#syntax) | Ninguno. Se permite el texto. |



 

## <a name="metadata"></a>metadata

Contenedor de elementos y texto que define los metadatos para el archivo determinado. Varios elementos de [metadatos](#syntax) pueden estar contenidos en un solo nodo de [archivo](#syntax) .

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

Define el destino de un lugar de red que se crea en **mis sitios de red** cuando se completa la carga. La creación de un lugar de red se puede evitar a través del método [**IPublishingWizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) .

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
| comment   | Obligatorio. El comentario que se muestra para el icono de ubicación de red cuando el cursor se sitúa sobre él.         |
| href      | Obligatorio. Dirección URL de la entrada de ubicación de red.                                                   |
| name      | Necesario. Nombre del icono de ubicación de red que aparece en la carpeta **mis sitios de red** . |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Ninguno. Se permite el texto. |



 

## <a name="post"></a>post

Dirección URL a la que se debe exponer el archivo. El servicio agrega este elemento cuando la transferencia se realiza como una publicación de varias partes y, con [formData](#syntax), se usa para compilar el encabezado post. Si el servicio elige realizar la transferencia de archivos mediante World Wide Web la creación y control de versiones distribuidas (WebDAV), no debería agregar este elemento. Varios elementos [post](#syntax) pueden estar contenidos en un solo nodo [File](#syntax) .

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
| nombreDeArchivo  | Opcional. Nombre del archivo expuesto.                                   |
| href      | Obligatorio. Dirección URL de la carpeta de destino.                                   |
| name      | Necesario. Define el nombre de datos del formulario asociado a esta sección de la publicación. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario  | Elementos secundarios      |
|-----------------|---------------------|
| [file](#syntax) | [formdata](#syntax) |



 

## <a name="resize"></a>resize

Define el escalado y la recompresión de un archivo de imagen en formato JPEG. Si el archivo de código fuente ya está en formato JPEG y es menor o igual que el ancho y el alto especificados, no se ajusta. Si el archivo de origen no es un archivo JPEG, se convierte. Se puede evitar el escalado, la recompresión y la conversión del archivo mediante el método [**IPublishingWizard:: Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ipublishingwizard-initialize) . Varios elementos de [tamaño](#syntax) pueden estar contenidos en un solo nodo de [archivo](#syntax) .

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
| serie        | Obligatorio. Ancho de la imagen, en píxeles, después de la carga. Si este valor es 0, **CX** se calcula a partir del valor **CY** para conservar las dimensiones relativas.  |
| cy        | Obligatorio. Alto de la imagen, en píxeles, después de la carga. Si este valor es 0, **CY** se calcula a partir del valor de **CX** para conservar las dimensiones relativas. |
| calidad   | Obligatorio. El valor de calidad JPEG, entre 0 y 100, y 100 es la calidad más alta.                                                                            |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario  | Elementos secundarios |
|-----------------|----------------|
| [file](#syntax) | Ninguno.          |



 

## <a name="successpage"></a>successpage

Especifica la página HTML del lado servidor que se va a mostrar si la carga se realiza correctamente.

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
| href      | Obligatorio. Dirección URL de la página HTML del servidor que se va a mostrar si la carga se realiza correctamente. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Ninguno. Se permite el texto. |



 

## <a name="target"></a>Destino

Una carpeta de destino especificada en el formato UNC (Convención de nomenclatura universal) o como servidor WebDAV. El servicio agrega este destino para especificar una carpeta de destino si la transferencia utiliza un protocolo WebDAV o de sistema de archivos. Si el servicio elige realizar la transferencia de archivos como una publicación de varias partes, no debe agregar este elemento.

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
| href      | Obligatorio. Dirección URL de la carpeta de destino. Use el formulario **https://** para WebDAV o el formulario de **\\ \\ \\ recurso compartido de servidor** para UNC. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario        | Elementos secundarios         |
|-----------------------|------------------------|
| [uploadinfo](#syntax) | Ninguno. Se permite el texto. |



 

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
| Ninguno           | [FileList](#syntax), [folderList](#syntax), [uploadinfo](#syntax) |



 

## <a name="uploadinfo"></a>uploadinfo

Contenedor de elementos que proporcionan información del sitio de carga utilizado en la transacción. Varios elementos [uploadinfo](#syntax) pueden estar contenidos en un único nodo [transfermanifest](#syntax) .

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
| FriendlyName | Obligatorio. Un nombre descriptivo para el sitio web que se muestra en el asistente. |



 

### <a name="element-information"></a>Información de elemento



| Elemento primario              | Elementos secundarios                                                                                                                                           |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [transfermanifest](#syntax) | [cancelledpage](#syntax), [failurepage](#syntax), [Favorite](#syntax), [htmlui](#syntax), [netplace](#syntax), [successpage](#syntax), [target](#syntax) |



 

 

 



