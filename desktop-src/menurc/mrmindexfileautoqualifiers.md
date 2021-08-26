---
title: Función MrmIndexFileAutoQualifiers (MrmResourceIndexer.h)
description: Indexa un archivo de recursos que pertenece a una aplicación para UWP. Deduce una lista de calificadores de recursos del parámetro filePath. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: CEA4D845-987C-48D6-B80E-9F055363FFE0
keywords:
- Menús y otros recursos de la función MrmIndexFileAutoQualifiers
topic_type:
- apiref
api_name:
- MrmIndexFileAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a10dbdb564f7e2d830d1edea59be6ca6f11b72d2650a937f96b6d305b6c7f61
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886735"
---
# <a name="mrmindexfileautoqualifiers-function"></a>Función MrmIndexFileAutoQualifiers

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Indexa un archivo de recursos que pertenece a una aplicación para UWP. Deduce una lista de calificadores de recursos del *parámetro filePath.* Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de [paquetes (PRI) y sistemas de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmIndexFileAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   filePath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexador* \[ En\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Identificador que identifica el indexador de recursos que indexará el archivo de recursos.

</dd> <dt>

*filePath* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

Ruta de acceso relativa a un archivo que contiene un recurso que desea indexar. Esta ruta de acceso es relativa a la raíz del proyecto de la aplicación para UWP para la que se generan archivos PRI. Esa raíz del proyecto es el valor *de projectRoot* que pasó a [**MrmCreateResourceIndexer.**](mrmcreateresourceindexer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

S \_ Ok si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

## <a name="remarks"></a>Comentarios

El segmento de nombre de archivo *de filePath* se usa como nombre del recurso; y los calificadores de recursos se derivan de su ruta de acceso. Por ejemplo, si pasa L"Images de-DE scale-100background.png" a filePath, el indexador de recursos agrega un recurso denominado "background.png" con calificadores de recursos \\ \\ \\ "language-de-DE" y "scale-100". 

L"Files" se usará como nombre del subárbol del mapa de recursos para este recurso cuando más adelante genere un archivo PRI a partir de este indexador de recursos.

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

 

