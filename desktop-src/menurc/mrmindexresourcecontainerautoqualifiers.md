---
title: Función MrmIndexResourceContainerAutoQualifiers (MrmResourceIndexer.h)
description: Indexa los recursos de cadena contenidos dentro de un archivo de recursos (.resw/.resjson) o un archivo .priinfo o .prifile, que pertenece a una aplicación para UWP.
ms.assetid: 7FCAA2B5-FF45-4961-84BA-B444B550C91D
keywords:
- Menús de función MrmIndexResourceContainerAutoQualifiers y otros recursos
topic_type:
- apiref
api_name:
- MrmIndexResourceContainerAutoQualifiers
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a05e05b9bbc6919d56760bec82e40989fac3a31bc57ad43712ccfddda3024e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952365"
---
# <a name="mrmindexresourcecontainerautoqualifiers-function"></a>Función MrmIndexResourceContainerAutoQualifiers

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Indexa los recursos de cadena contenidos dentro de un archivo de recursos (.resw/.resjson) o un archivo .priinfo o .prifile, que pertenece a una aplicación para UWP. Deduce una lista de calificadores de recursos del *parámetro containerPath.* Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmIndexResourceContainerAutoQualifiers(
  _In_ MrmResourceIndexerHandle indexer,
  _In_ PCWSTR                   containerPath
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexador* \[ En\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Identificador que identifica el indexador de recursos que indexará los recursos de cadena.

</dd> <dt>

*containerPath* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

Ruta de acceso relativa a un archivo .resw, .resjson, .priinfo o .prifile que contiene los recursos de cadena que desea indexar. Esta ruta de acceso es relativa a la raíz del proyecto de la aplicación para UWP para la que se generan archivos PRI. Esa raíz del proyecto es el valor *de projectRoot* que pasó a [**MrmCreateResourceIndexer.**](mrmcreateresourceindexer.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Es \_ correcto si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

## <a name="remarks"></a>Comentarios

Los calificadores de recursos se deducen de *containerPath.* Por ejemplo, un valor de L"en-US resources.resw" agrega recursos de cadena con el \\ \\ calificador "language-en-US".

El nombre del archivo de recursos se usará como nombre del subárbol del mapa de recursos para estos recursos cuando más adelante genere un archivo PRI a partir de este indexador de recursos.

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

 

