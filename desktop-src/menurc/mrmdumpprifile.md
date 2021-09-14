---
title: Función MrmDumpPriFile (MrmResourceIndexer.h)
description: Vuelca un archivo PRI (que es binario) en su equivalente XML (como un archivo en disco) para que sea más fácil de leer.
ms.assetid: FE1982AB-881C-4F07-8B9E-E3770E5B5099
keywords:
- Menús de la función MrmDumpPriFile y otros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba254cbac0dd8afd328e0d7e04f573138f14b588
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248457"
---
# <a name="mrmdumpprifile-function"></a>Función MrmDumpPriFile

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Vuelca un archivo PRI (que es binario) en su equivalente XML (como un archivo en disco) para que sea más fácil de leer. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmDumpPriFile(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _In_     PCWSTR      outputXmlFile
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexFileName* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

Una ruta de acceso de archivo completa a un archivo PRI. Este es el archivo PRI que se volcará en XML.

</dd> <dt>

*schemaPriFile* \[ en, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Una ruta de acceso de archivo completa opcional a un archivo de esquema (o a un archivo PRI que representa un esquema; vea Comentarios).

</dd> <dt>

*dumpType* \[ En\]
</dt> <dd>

Tipo: **[ **MrmDumpType**](mrmdumptype.md)**

Especifica lo detallado que debe ser el volcado XML o si se debe volcar un esquema.

</dd> <dt>

*outputXmlFile* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

Ruta de acceso de un archivo XML que se creará.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

S \_ Ok si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

## <a name="remarks"></a>Observaciones

Un paquete de recursos sin esquema es aquel que se creó con el argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) pasado a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (o con el *modificador omitSchemaFromResourcePacks* en el archivo de configuración de PRI). Para volcar un paquete de recursos sin esquema, pase la ruta de acceso a los datos de PRI del paquete principal como argumento para el *parámetro schemaPriFile.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de servidor\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

