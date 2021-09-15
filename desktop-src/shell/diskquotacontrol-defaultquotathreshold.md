---
description: Establece u obtiene el umbral de cuota predeterminado.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: Propiedad DiskQuotaControl.DefaultQuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a4ce4205ee8bcc73c78bd1aabe7d8659ac3f5489
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468259"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a>Propiedad DiskQuotaControl.DefaultQuotaThreshold

Establece u obtiene el umbral de cuota predeterminado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a>Valor de propiedad

Valor **entero** que se establece en el umbral de advertencia predeterminado para los nuevos usuarios, en bytes.

## <a name="remarks"></a>Observaciones

El umbral de cuota predeterminado se aplica automáticamente a los nuevos usuarios del volumen. Si el uso del disco de un usuario supera este valor y la propiedad [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) se establece en **TRUE,** el sistema genera una entrada del registro de eventos. Por ejemplo, si el umbral predeterminado es 10,0 MB, el valor de la propiedad es "10,0 MB". Si el volumen no tiene ningún umbral predeterminado, la propiedad se establece en "Sin límite" o en el equivalente localizado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




