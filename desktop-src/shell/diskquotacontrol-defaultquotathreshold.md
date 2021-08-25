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
ms.openlocfilehash: 46d44f2e2df24c5ee1cbf646643810e09d007eb15ba6c9a352eb492dfb104752
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943115"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a>Propiedad DiskQuotaControl.DefaultQuotaThreshold

Establece u obtiene el umbral de cuota predeterminado.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a>Valor de propiedad

Valor **entero** que se establece en el umbral de advertencia predeterminado para los nuevos usuarios, en bytes.

## <a name="remarks"></a>Comentarios

El umbral de cuota predeterminado se aplica automáticamente a los nuevos usuarios del volumen. Si el uso de disco de un usuario supera este valor y la propiedad [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) se establece en **TRUE,** el sistema genera una entrada del registro de eventos. Por ejemplo, si el umbral predeterminado es 10,0 MB, el valor de la propiedad es "10,0 MB". Si el volumen no tiene ningún umbral predeterminado, la propiedad se establece en "Sin límite" o en el equivalente localizado.

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

 

 




