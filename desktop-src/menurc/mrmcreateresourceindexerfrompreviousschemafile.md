---
title: Función MrmCreateResourceIndexerFromPreviousSchemaFile (MrmResourceIndexer.h)
description: Crea un indexador de recursos a partir de un archivo de esquema creado con una llamada anterior a MrmDumpPriFile. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: 2ECF355C-C6FD-4949-B455-52E3FF455005
keywords:
- Menús de la función MrmCreateResourceIndexerFromPreviousSchemaFile y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousSchemaFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 622fe76c9206b4a8223d27d810f3d02bc0dca1d08730623b595ead24eab719d6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847375"
---
# <a name="mrmcreateresourceindexerfrompreviousschemafile-function"></a>Función MrmCreateResourceIndexerFromPreviousSchemaFile

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Crea un indexador de recursos a partir de un archivo de esquema creado con una llamada anterior a [**MrmDumpPriFile**](mrmdumpprifile.md). Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousSchemaFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   schemaFile,
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

*schemaFile* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

Ruta de acceso completa a un archivo de esquema creado por una llamada anterior a [**MrmDumpPriFile**](mrmdumpprifile.md).

</dd> <dt>

*indexador* \[ in, out\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\***

Puntero a un identificador de indexador de recursos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

S \_ Ok si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

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

 

