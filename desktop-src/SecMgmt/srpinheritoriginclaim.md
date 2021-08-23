---
description: Esta función toma el atributo de origen si está presente del token de origen y los establece en un duplicado del token de herencia y devuelve el token duplicado.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: Función srpInheritOriginClaim
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- srpInheritOriginClaim
api_type:
- DllExport
api_location:
- srpapi.dll
ms.openlocfilehash: 64436c699f5cb24b2a12675342078242a340fb2e53de3a6a8f3224d8b88beac0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004902"
---
# <a name="srpinheritoriginclaim-function"></a>Función srpInheritOriginClaim

\[Parte de la información está relacionada con el producto publicado previamente que se puede modificar considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Esta función toma el atributo de origen si está presente del token de origen y los establece en un duplicado del token de herencia y devuelve el token duplicado. A continuación, el autor de la llamada puede suplantar el token devuelto. Esta función no tiene ninguna biblioteca de importación asociada. Debe usar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a srpapi.dll.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT WINAPI srpInheritOriginClaim(
  _In_ Handle OriginToken,
  _In_ Handle InheritingToken,
       Handle ResultToken
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*OriginToken* \[ En\]
</dt> <dd>

Identificador del token que está duplicado y recibe el atributo de origen heredado. Este identificador debe abrirse con el derecho de acceso TOKEN \_ DUPLICATE.

</dd> <dt>

*InheritingToken* \[ En\]
</dt> <dd>

Identificador del token que está duplicado y recibe el atributo de origen heredado. Este identificador debe abrirse con el derecho de acceso TOKEN \_ DUPLICATE. 

</dd> <dt>

*ResultToken* 
</dt> <dd>

Si se ejecuta correctamente, recibe el token duplicado. El autor de la llamada puede suplantarlo para realizar operaciones con el atributo de origen heredado. El autor de la llamada toma posesión de este identificador y debe cerrarlo. 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                           |
| Servidor mínimo compatible<br/> | \[Windows Server 2016 solo aplicaciones de escritorio\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Srpapi.dll</dt> </dl> |



 

