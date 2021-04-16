---
description: Esta función toma el atributo Origin si está presente desde el token de origen y lo establece en un duplicado del token que hereda, y devuelve el token duplicado.
ms.assetid: ED1FAEA1-0665-49FA-BD8B-232254B4C883
title: srpInheritOriginClaim función)
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
ms.openlocfilehash: 3edf274622bc1a2611bc49d710a809bd80bd501a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686674"
---
# <a name="srpinheritoriginclaim-function"></a>srpInheritOriginClaim función)

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Esta función toma el atributo Origin si está presente desde el token de origen y lo establece en un duplicado del token que hereda, y devuelve el token duplicado. Después, el autor de la llamada puede suplantar el token devuelto. Esta función no tiene ninguna biblioteca de importación asociada. Debe utilizar las funciones [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) y [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) para vincular dinámicamente a srpapi.dll.

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

*OriginToken* \[ de\]
</dt> <dd>

Identificador del token que está duplicado y recibe el atributo de origen heredado. Este identificador debe abrirse con el derecho de acceso de TOKEN \_ duplicado.

</dd> <dt>

*InheritingToken* \[ de\]
</dt> <dd>

Identificador del token que está duplicado y recibe el atributo de origen heredado. Este identificador debe abrirse con el derecho de acceso de TOKEN \_ duplicado. 

</dd> <dt>

*ResultToken* 
</dt> <dd>

Si se ejecuta correctamente, recibe el token duplicado. El autor de la llamada puede suplantarlo para realizar operaciones con el atributo de origen heredado. El autor de la llamada toma la propiedad de este identificador y debe cerrarlo. 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si esta función se ejecuta correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2016 \[\]<br/>                                  |
| Archivo DLL<br/>                      | <dl> <dt>Srpapi.dll</dt> </dl> |



 

