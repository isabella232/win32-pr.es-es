---
description: Obtiene el umbral de cuota predeterminado como una cadena de texto.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: Propiedad DiskQuotaControl.DefaultQuotaThresholdText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127579613"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a>Propiedad DiskQuotaControl.DefaultQuotaThresholdText

Obtiene el umbral de cuota predeterminado como una cadena de texto.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a>Valor de propiedad

Valor de cadena que contiene el umbral de cuota predeterminado para el volumen.

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

 

 




