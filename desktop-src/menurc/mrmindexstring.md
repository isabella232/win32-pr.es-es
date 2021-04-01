---
title: Función MrmIndexString (MrmResourceIndexer. h)
description: Indexa un recurso de cadena único que pertenece a una aplicación de UWP.
ms.assetid: 098F47E7-4BEC-452F-A33C-111F3F524E67
keywords:
- Menús de la función MrmIndexString y otros recursos
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
ms.openlocfilehash: ec0c81155ae2484dd38f29e332a5f0093b07cd9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149948"
---
# <a name="mrmindexstring-function"></a>MrmIndexString función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Indexa un recurso de cadena único que pertenece a una aplicación de UWP. Toma una lista explícita (pero opcional) de calificadores de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

*indexador* \[ de\]
</dt> <dd>

Tipo: **[ **MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)**

Identificador que identifica el indizador de recursos que indizará los recursos de cadena.

</dd> <dt>

*resourceUri* \[ de\]
</dt> <dd>

Tipo: **PCWSTR**

URI de recurso que se va a asignar al recurso. La ruta de acceso se usará como el nombre del subárbol del mapa de recursos para este recurso cuando se genere posteriormente un archivo PRI a partir de este indexador de recursos.

</dd> <dt>

*resourceString* \[ de\]
</dt> <dd>

Tipo: **PCWSTR**

Valor del recurso de cadena.

</dd> <dt>

*calificadores* \[ en, opcional\]
</dt> <dd>

Tipo: **PCWSTR**

Una lista opcional de calificadores de recursos, por ejemplo, L "Language-en-US \_ Scale-100 \_ Contrast-Standard". Una cadena vacía o **nullptr** indica un recurso neutro. Los calificadores de recursos *no* se deducen de *resourceUri*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Es \_ correcto si la función se realizó correctamente; de lo contrario, es algún otro valor. Use las macros SUCCEEDED () o FAILed () (definidas en Winerror. h) para determinar si la operación se ha realizado correctamente o no.

## <a name="remarks"></a>Observaciones

Si desea especificar los calificadores de recursos, páselo en el parámetro *calificadores* . Los calificadores de recursos *no* se deducen de *resourceUri*.

El segmento de nombre de archivo de *resourceUri* se usa como nombre del recurso.

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

 

