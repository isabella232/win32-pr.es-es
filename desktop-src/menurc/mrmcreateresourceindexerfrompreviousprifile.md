---
title: Función MrmCreateResourceIndexerFromPreviousPriFile (MrmResourceIndexer. h)
description: Crea un indizador de recursos a partir de un archivo PRI creado con una llamada anterior a MrmCreateResourceFile. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: 8B3743EF-1A27-4B70-9577-8549B91DBC1E
keywords:
- Menús de la función MrmCreateResourceIndexerFromPreviousPriFile y otros recursos
topic_type:
- apiref
api_name:
- MrmCreateResourceIndexerFromPreviousPriFile
api_location:
- Mrmsupport.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be08170dc8ae25db34492273e7c612352d5e0530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105666009"
---
# <a name="mrmcreateresourceindexerfrompreviousprifile-function"></a>MrmCreateResourceIndexerFromPreviousPriFile función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Crea un indizador de recursos a partir de un archivo PRI creado con una llamada anterior a [**MrmCreateResourceFile**](mrmcreateresourcefile.md). Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT HRESULT MrmCreateResourceIndexerFromPreviousPriFile(
  _In_     PCWSTR                   projectRoot,
  _In_     MrmPlatformVersion       platformVersion,
  _In_opt_ PCWSTR                   defaultQualifiers,
  _In_     PCWSTR                   priFile,
  _Inout_  MrmResourceIndexerHandle *indexer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*projectRoot* \[ de\]
</dt> <dd>

Tipo: **PCWSTR**

La raíz del proyecto de la aplicación para UWP para la que va a generar archivos PRI. En otras palabras, la ruta de acceso a los archivos de recursos de esa aplicación. Especifique esto para que pueda especificar las rutas de acceso relativas a esa raíz en las posteriores llamadas API al mismo indexador de recursos.

</dd> <dt>

*platformVersion* \[ de\]
</dt> <dd>

Tipo: **[ **MrmPlatformVersion**](mrmplatformversion.md)**

Versión de la plataforma de destino para el indizador de recursos.

</dd> <dt>

*defaultQualifiers* \[ en, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Una lista de calificadores de recursos predeterminados. Por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard"

</dd> <dt>

*priFile* \[ de\]
</dt> <dd>

Tipo: **PCWSTR**

Ruta de acceso completa a un archivo PRI.

</dd> <dt>

*indexador* \[ in, out\]
</dt> <dd>

Tipo: **[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) \** _

Un puntero a un identificador de indizador de recursos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: _ *HRESULT**

Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor. Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server \[\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>Mrmsupport. lib</dt> </dl>       |
| Archivo DLL<br/>                      | <dl> <dt>Mrmsupport.dll</dt> </dl>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

