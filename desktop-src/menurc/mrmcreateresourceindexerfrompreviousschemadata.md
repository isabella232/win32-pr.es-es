---
title: Función MrmCreateResourceIndexerFromPreviousSchemaData (MrmResourceIndexer.h)
description: Crea un indexador de recursos a partir de datos de esquema en memoria creados con una llamada anterior a MrmDumpPriFileInMemory o MrmDumpPriDataInMemory.
ms.assetid: D9C90C12-CEFE-4794-9553-8BFBE9E43D99
keywords:
- Menús de la función MrmCreateResourceIndexerFromPreviousSchemaData y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaData
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcc0ece1d46a6e9a3ec57fe7b9fb074b4a0a01fd53217c67ed44f49573383588
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687311"
---
# <a name="mrmcreateresourceindexerfrompreviousschemadata-function"></a>Función MrmCreateResourceIndexerFromPreviousSchemaData

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Crea un indexador de recursos a partir de datos de esquema en memoria creados con una llamada anterior a [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) o [**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md). Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de [paquetes (PRI) y sistemas de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaData(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     BYTE                     *schemaXmlData,
  _In_     ULONG                    schemaXmlSize,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*projectRoot* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

La raíz del proyecto de la aplicación para UWP para la que va a generar archivos PRI. En otras palabras, la ruta de acceso a los archivos de recursos de esa aplicación. Especifique esto para que pueda especificar rutas de acceso relativas a esa raíz en las llamadas API posteriores al mismo indexador de recursos.

</dd> <dt>

*platformVersion* \[ En\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Versión de la plataforma de destino para el indexador de recursos.

</dd> <dt>

*defaultQualifiers* \[ en, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Lista de calificadores de recursos predeterminados. Por ejemplo, L"language-en-US \_ scale-100 \_ contrast-standard"

</dd> <dt>

*schemaXmlData* \[ En\]
</dt> <dd>

Tipo: **\* BYTE**

Puntero a los datos de esquema creados por una llamada anterior a [**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) [**o MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md). No liberar *schemaXmlData hasta* que haya terminado de usar el indexador de recursos creado por esta función.

</dd> <dt>

*schemaXmlSize* \[ En\]
</dt> <dd>

Tipo: **ULONG**

Tamaño de los datos a los que apunta *schemaXmlData.*

</dd> <dt>

*indexador* \[ in, out\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\***

Puntero a un identificador de indexador de recursos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

S \_ Ok si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

## <a name="remarks"></a>Comentarios

No liberar *schemaXmlData hasta* que haya terminado de usar el indexador de recursos creado por esta función.

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

 

