---
description: Obtiene el límite de cuota predeterminado como una cadena de texto.
title: Propiedad DiskQuotaControl.DefaultQuotaLimitText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 378d06286a0334cf6ca3056038f45be3a5919b4fd2aa88934957122bc751c141
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119094236"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a>Propiedad DiskQuotaControl.DefaultQuotaLimitText

Obtiene el límite de cuota predeterminado como una cadena de texto.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a>Valor de propiedad

Valor de cadena que contiene el límite de cuota predeterminado para los nuevos usuarios del volumen. Por ejemplo, si la cuota predeterminada es de 10,5 MB, el valor de la propiedad es "10,5 MB". Si el volumen no tiene ninguna cuota predeterminada, la propiedad se establece en "Sin límite" o en el equivalente localizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DefaultQuotaLimit**](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




