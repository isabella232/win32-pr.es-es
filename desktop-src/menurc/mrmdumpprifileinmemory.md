---
title: Función MrmDumpPriFileInMemory (MrmResourceIndexer.h)
description: Vuelca un archivo PRI (que es binario) en su equivalente XML (como datos en memoria) para que sea más fácil de leer.
ms.assetid: 04FD048F-1473-47B1-9CAB-03FEF98A9B48
keywords:
- Menús de la función MrmDumpPriFileInMemory y otros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriFileInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c591f95b772d71fd0ce614598bbf793d84dff70a0c29664da460c8be33569d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120092155"
---
# <a name="mrmdumpprifileinmemory-function"></a>Función MrmDumpPriFileInMemory

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Vuelca un archivo PRI (que es binario) en su equivalente XML (como datos en memoria) para que sea más fácil de leer. La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData.* Llame [**a MrmFreeMemory con**](mrmfreememory.md) el mismo puntero para liberar esa memoria. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmDumpPriFileInMemory(
  _In_     PCWSTR      indexFileName,
  _In_opt_ PCWSTR      schemaPriFile,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexFileName* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

Ruta de acceso de archivo completa a un archivo PRI. Este es el archivo PRI que se va a volcar en XML.

</dd> <dt>

*schemaPriFile* \[ in, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Una ruta de acceso de archivo completa opcional a un archivo de esquema (o a un archivo PRI que representa un esquema; vea Comentarios).

</dd> <dt>

*dumpType* \[ En\]
</dt> <dd>

Tipo: **[ **MrmDumpType**](mrmdumptype.md)**

Especifica lo detallado que debe ser el volcado XML o si se debe volcar un esquema.

</dd> <dt>

*outputXmlData* \[ out\]
</dt> <dd>

Tipo: **\* \* BYTE**

Dirección de un puntero a BYTE. La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData.* Llame [**a MrmFreeMemory con**](mrmfreememory.md) el puntero a BYTE para liberar esa memoria.

</dd> <dt>

*outputXmlSize* \[ out\]
</dt> <dd>

Tipo: **ULONG \***

Dirección de un ULONG. En *outputXmlSize*, la función devuelve el tamaño de la memoria asignada a la que *apunta outputXmlData.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Es \_ correcto si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

## <a name="remarks"></a>Comentarios

Un paquete de recursos sin esquema es el que se creó con el argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) pasado a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (o con el *modificador omitSchemaFromResourcePacks* en el archivo de configuración de PRI). Para volcar un paquete de recursos sin esquema, pase la ruta de acceso a los datos de PRI del paquete principal como argumento para el *parámetro schemaPriFile.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de servidor\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

