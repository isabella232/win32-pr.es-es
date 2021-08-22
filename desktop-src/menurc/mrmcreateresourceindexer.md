---
title: Función MrmCreateResourceIndexer (MrmResourceIndexer.h)
description: Crea un indexador de recursos, que se usa para generar archivos de índice de recursos de paquete (PRI) para una aplicación para UWP. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: 9AE3EF90-4ADC-4646-9C62-87A702333B9A
keywords:
- Menús de función MrmCreateResourceIndexer y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexer
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d427163862d084c4a386fdf47cbd8586cb1a3489b18fb081471fbd31c86854b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119601815"
---
# <a name="mrmcreateresourceindexer-function"></a>Función MrmCreateResourceIndexer

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Crea un indexador de recursos, que se usa para generar archivos de índice de recursos de paquete (PRI) para una aplicación para UWP. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmCreateResourceIndexer(
  _In_     PCWSTR                   packageFamilyName,
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*packageFamilyName* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

Nombre de familia del paquete de la aplicación para UWP para la que va a generar archivos PRI. Este valor se usará como nombre del mapa de recursos cuando más adelante genere un archivo PRI a partir de este indexador de recursos.

</dd> <dt>

*projectRoot* \[ En\]
</dt> <dd>

Tipo: **PCWSTR**

La raíz del proyecto de la aplicación para UWP para la que va a generar archivos PRI. En otras palabras, la ruta de acceso a los archivos de recursos de esa aplicación. Especifique esto para que pueda especificar rutas de acceso relativas a esa raíz en llamadas API posteriores al mismo indexador de recursos.

</dd> <dt>

*platformVersion* \[ En\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Versión de la plataforma de destino para el indexador de recursos.

</dd> <dt>

*defaultQualifiers* \[ in, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Lista de calificadores de recursos predeterminados. Por ejemplo, L"language-en-US \_ scale-100 \_ contrast-standard"

</dd> <dt>

*indexador* \[ in, out\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)\***

Puntero a un identificador de indexador de recursos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Es \_ correcto si la función se ha hecho correctamente; de lo contrario, algún otro valor. Use las macros SUCCEEDED() o FAILED() (definidas en winerror.h) para determinar el éxito o el error.

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

 

