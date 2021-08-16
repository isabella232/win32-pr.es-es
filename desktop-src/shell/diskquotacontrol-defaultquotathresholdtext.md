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
ms.openlocfilehash: 8f16c32b46544d3966ae5e3a097576074d28bcfa40ce568cd591d37f9d3d0552
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459908"
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

## <a name="remarks"></a>Comentarios

El umbral de cuota predeterminado se aplica automáticamente a los nuevos usuarios del volumen. Si el uso del disco de un usuario supera este valor y la propiedad [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) se establece en **TRUE,** el sistema genera una entrada del registro de eventos. Por ejemplo, si el umbral predeterminado es 10,0 MB, el valor de la propiedad es "10,0 MB". Si el volumen no tiene ningún umbral predeterminado, la propiedad se establece en "Sin límite" o en el equivalente localizado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




