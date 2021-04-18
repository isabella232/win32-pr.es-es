---
title: DownloadCollection. startDownload, método
description: Tenga en cuenta que en esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea. El método startDownload pone en cola una descarga.
ms.assetid: 54cf91fe-cef9-4424-9f99-629e773eade1
keywords:
- método startDownload de Windows Media Player
- método startDownload de Windows Media Player, clase DownloadCollection
- Clase DownloadCollection Windows Media Player, método startDownload
topic_type:
- apiref
api_name:
- DownloadCollection.startDownload
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d3187ce00dda45f7e4660b4961c78af6db2af50e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105700085"
---
# <a name="downloadcollectionstartdownload-method"></a>DownloadCollection. startDownload, método

> [!Note]  
> En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea. No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.

 

El método **startDownload** pone en cola una descarga.

## <a name="syntax"></a>Sintaxis


```JScript
retVal = DownloadCollection.startDownload(
  sourceURL,
  type
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*sourceURL* \[ de\]
</dt> <dd>

**Cadena** que especifica la dirección URL de la descarga.

</dd> <dt>

*tipo* \[ de de\]
</dt> <dd>

**Cadena** que especifica el tipo de descarga. Contiene uno de los valores siguientes.



| Value      | Descripción                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| background | (Windows XP y versiones posteriores). La descarga se produce como un proceso en segundo plano a medida que el tiempo de procesador está disponible. Los Estados de descarga se conservan incluso cuando se apaga Windows Media Player o Windows XP. |
| en tiempo real  | (Todos los sistemas operativos compatibles). La descarga se produce a la vez. No se conservan los Estados de descarga entre sesiones.                                                                            |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve un objeto **DownloadItem** .

## <a name="remarks"></a>Observaciones

Cuando se inicia una nueva descarga, Download Manager la agrega como un elemento a la colección de descarga que inició la descarga.

Solo se pueden descargar los siguientes formatos de medios digitales:

-   Formato ASF
-   MP3
-   Audio de Windows Media (WMA)
-   Vídeo de Windows Media (WMV)

El parámetro *sourceURL* no admite cadenas con codificación Unicode. Debe apuntar a contenido válido. No se admiten las redirecciones.

Cuando se usa Windows XP, los archivos de audio se colocan automáticamente en sus subcarpetas de **música** apropiadas según los valores de metadatos de nivel de archivo. Los archivos de vídeo se colocan en \\ el \\ \\  \\ *tipo* de número aleatorio de descarga de música, donde el *número aleatorio* es un valor aleatorio generado por Windows Media Player para cada usuario, y el *tipo* es "en tiempo real" o "en segundo plano", en función del tipo de descarga.

Cuando se usa Windows Media Player 9 series con Windows 98 y Windows Millennium Edition (me), los archivos de audio y vídeo se colocan en el \\ \\ \\  \\ *tipo* de número aleatorio de descarga de música, donde el *número aleatorio* es un valor aleatorio generado por el reproductor para cada usuario y el *tipo* es "tiempo real" o "fondo", dependiendo del tipo de descarga.

Tenga en cuenta que se puede cambiar el nombre de los archivos en función de los atributos de metadatos contenidos en el archivo y las reglas especificadas por el usuario en el cuadro de diálogo **Opciones** . Los archivos que no contienen metadatos, como **álbum** o **intérprete**, pueden moverse a carpetas etiquetadas como intérprete desconocido o álbum desconocido.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|------------------------------------------------------------------------------------|
| Versión<br/> | Windows Media Player 9 series o posterior<br/>                                  |
| Archivo DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto DownloadCollection**](downloadcollection-object.md)
</dt> <dt>

[**Objeto DownloadItem**](downloaditem-object.md)
</dt> </dl>

 

 





