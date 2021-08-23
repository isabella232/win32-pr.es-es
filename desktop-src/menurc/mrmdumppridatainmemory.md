---
title: Función MrmDumpPriDataInMemory (MrmResourceIndexer.h)
description: Vuelca la información de PRI (como un blob en memoria, creado por una llamada anterior a MrmCreateResourceFileInMemory) en su equivalente XML (como datos en memoria), con el fin de que sea más fácil de leer.
ms.assetid: 6E563B43-4E0A-465D-A8EA-7DE61738DE06
keywords:
- Menús de la función MrmDumpPriDataInMemory y otros recursos
topic_type:
- apiref
api_name:
- MrmDumpPriDataInMemory
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dbeec26f0741ebb77b742ff647e91cb5fd18afe633a1519228b887b4b438bb72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601785"
---
# <a name="mrmdumppridatainmemory-function"></a>Función MrmDumpPriDataInMemory

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Vuelca la información de PRI (como un blob en memoria, creado por una llamada anterior a [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)) en su equivalente XML (como datos en memoria), con el fin de que sea más fácil de leer. La función asigna memoria y devuelve un puntero a esa memoria en *outputXmlData.* Llame [**a MrmFreeMemory con**](mrmfreememory.md) el mismo puntero para liberar esa memoria. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmDumpPriDataInMemory(
  _In_     BYTE        *inputPriData,
  _In_     ULONG       inputPriSize,
  _In_opt_ BYTE        *schemaPriData,
  _In_     ULONG       schemaPriSize,
  _In_     MrmDumpType dumpType,
  _Out_    BYTE        **outputXmlData,
  _Out_    ULONG       *outputXmlSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*inputPriData* \[ En\]
</dt> <dd>

Tipo: **\* BYTE**

Puntero a los datos de PRI creados por una llamada anterior a [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md).

</dd> <dt>

*inputPriSize* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Tamaño de los datos a los que apunta *inputPriData.*

</dd> <dt>

*schemaPriData* \[ en, opcional\]
</dt> <dd>

Tipo: **\* BYTE**

Puntero opcional a la información de PRI (como un blob en memoria) que representa los datos de esquema creados por una llamada anterior a [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md). No liberar *schemaPriData hasta* que haya terminado de usar el indexador de recursos. Consulte también Comentarios.

</dd> <dt>

*schemaPriSize* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Tamaño de los datos a los que apunta *schemaPriData.*

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

Dirección de un ULONG. En *outputXmlSize*, la función devuelve el tamaño de la memoria asignada a la que *apunta outputXmlData*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

S \_ Ok si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

## <a name="remarks"></a>Comentarios

Un paquete de recursos sin esquema es aquel que se creó con el argumento [**MrmPackagingOptionsOmitSchemaFromResourcePacks**](mrmpackagingoptions.md) pasado a [**MrmCreateResourceFile**](mrmcreateresourcefile.md) o [**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) (o con el *modificador omitSchemaFromResourcePacks* en el archivo de configuración de PRI). Para volcar un paquete de recursos sin esquema, pase la ruta de acceso a los datos de PRI del paquete principal como argumento para el *parámetro schemaPriData.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

