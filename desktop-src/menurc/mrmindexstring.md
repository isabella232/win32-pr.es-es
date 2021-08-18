---
title: Función MrmIndexString (MrmResourceIndexer.h)
description: Indexa un recurso de cadena única que pertenece a una aplicación para UWP.
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- Menús de función MrmIndexString y otros recursos
topic_type:
- apiref
api_name:
- MrmIndexString
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99da5b63c08d0068553ca9240798eabe360671fa94139b31841831dd68df3958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687257"
---
# <a name="mrmindexstring-function"></a>Función MrmIndexString

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Indexa un recurso de cadena única que pertenece a una aplicación para UWP. Toma una lista explícita (pero opcional) de calificadores de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmIndexString(
  _In_     MrmResourceIndexerHandle indexer,
  _In_     PCWSTR                   resourceUri,
  _In_     PCWSTR                   resourceString,
  _In_opt_ PCWSTR                   qualifiers
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*indexador* \[ En\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Identificador que identifica el indexador de recursos que indexará los recursos de cadena.

</dd> <dt>

*resourceUri* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

URI del recurso que se asignará al recurso. La ruta de acceso se usará como nombre del subárbol del mapa de recursos para este recurso cuando más adelante genere un archivo PRI a partir de este indexador de recursos.

</dd> <dt>

*resourceString* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

Valor del recurso de cadena.

</dd> <dt>

*calificadores* \[ in, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Lista opcional de calificadores de recursos, por ejemplo, L"language-en-US \_ scale-100 \_ contrast-standard". Una cadena vacía o **nullptr** indica un recurso neutro. Los calificadores de recursos *no se* deducen *de resourceUri.*

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

S \_ Ok si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

## <a name="remarks"></a>Comentarios

Si desea especificar los calificadores de recursos, pásenlos en el parámetro *qualifiers.* Los calificadores de recursos *no se* deducen *de resourceUri.*

El segmento de nombre de archivo *de resourceUri* se usa como nombre del recurso.

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

 

