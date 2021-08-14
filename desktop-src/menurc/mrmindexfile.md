---
title: Función MrmIndexFile (MrmResourceIndexer.h)
description: Indexa un archivo de recursos que pertenece a una aplicación para UWP. Toma una lista explícita (pero opcional) de calificadores de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: C9F245B4-D2D3-4863-BB64-72619FC73D3C
keywords:
- Menús de la función MrmIndexFile y otros recursos
topic_type:
- apiref
api_name:
- MrmIndexFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 004e8d81f3af7d0aa7844ed5661f71713db3f7fc49616fba0d56bed833a87f0a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118733685"
---
# <a name="mrmindexfile-function"></a>Función MrmIndexFile

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Indexa un archivo de recursos que pertenece a una aplicación para UWP. Toma una lista explícita (pero opcional) de calificadores de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de [paquetes (PRI) y sistemas de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmIndexFile(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   filePath,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexador* \[ En\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Identificador que identifica el indexador de recursos que indexará el archivo de recursos.

</dd> <dt>

*resourceUri* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

Uri de recurso que se asignará al recurso. La ruta de acceso se usará como el nombre del subárbol del mapa de recursos para este recurso cuando más adelante genere un archivo PRI a partir de este indexador de recursos.

</dd> <dt>

*filePath* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

Ruta de acceso relativa a un archivo que contiene un recurso que desea indexar. Esta ruta de acceso es relativa a la raíz del proyecto de la aplicación para UWP para la que se generan archivos PRI. Esa raíz del proyecto es el valor *de projectRoot* que pasó a [**MrmCreateResourceIndexer.**](mrmcreateresourceindexer.md)

</dd> <dt>

*calificadores* \[ en, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Una lista opcional de calificadores de recursos, por ejemplo, L"language-en-US \_ scale-100 \_ contrast-standard". Una cadena vacía o **nullptr** indica un recurso neutro. Los calificadores de recursos *no se* deducen de *resourceUri* ni de *containerPath.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

S \_ Ok si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

## <a name="remarks"></a>Comentarios

Si desea especificar los calificadores de recursos, pásenlos en el parámetro *qualifiers.* Los calificadores de recursos *no se* deducen de *resourceUri* ni de *filePath.*

El segmento de nombre de archivo *de resourceUri* (no *filePath*) se usa como nombre del recurso.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de servidor\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport.lib</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

