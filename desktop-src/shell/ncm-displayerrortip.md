---
description: Muestra un mensaje de error en el globo de sugerencias asociado con el control de dirección de red.
title: Mensaje de NCM_DISPLAYERRORTIP (ShellAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997256"
---
# <a name="ncm_displayerrortip-message"></a>NCM \_ DISPLAYERRORTIP

Muestra un mensaje de error en el globo de sugerencias asociado con el control de dirección de red.


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>Debe ser cero.</dd> <dt>

*lParam* 
</dt> <dd>Debe ser cero.</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este mensaje se realiza correctamente, devuelve **S \_ correcto**. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Envía este mensaje para mostrar un mensaje de error cuando una dirección escrita en el control no se valida con respecto a los tipos de direcciones de red permitidos establecidos con el mensaje [**\_ SETALLOWTYPE de NCM**](ncm-setallowtype.md) . Use el mensaje de [**NCM \_ GETADDRESS**](ncm-getaddress.md) para validar la dirección.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>ShellAPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**NetAddr \_ DisplayErrorTip**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




