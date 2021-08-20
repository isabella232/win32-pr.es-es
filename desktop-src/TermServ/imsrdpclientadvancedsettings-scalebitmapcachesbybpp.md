---
title: Propiedad IMsRdpClientAdvancedSettings ScaleBitmapCachesByBPP
description: Esta propiedad no es compatible. | Propiedad IMsRdpClientAdvancedSettings ScaleBitmapCachesByBPP
ms.assetid: 1da3d634-6322-4546-92cf-5607dc74d400
ms.tgt_platform: multiple
keywords:
- Propiedad ScaleBitmapCachesByBPP Servicios de Escritorio remoto
- Propiedad ScaleBitmapCachesByBPP Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings
- Interfaz IMsRdpClientAdvancedSettings Servicios de Escritorio remoto , propiedad ScaleBitmapCachesByBPP
- Propiedad ScaleBitmapCachesByBPP Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings2
- Interfaz IMsRdpClientAdvancedSettings2 Servicios de Escritorio remoto , propiedad ScaleBitmapCachesByBPP
- Propiedad ScaleBitmapCachesByBPP Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings3
- Interfaz IMsRdpClientAdvancedSettings3 Servicios de Escritorio remoto , propiedad ScaleBitmapCachesByBPP
- Propiedad ScaleBitmapCachesByBPP Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings4
- Interfaz IMsRdpClientAdvancedSettings4 Servicios de Escritorio remoto , propiedad ScaleBitmapCachesByBPP
- Propiedad ScaleBitmapCachesByBPP Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings5
- Interfaz IMsRdpClientAdvancedSettings5 Servicios de Escritorio remoto , propiedad ScaleBitmapCachesByBPP
- Propiedad ScaleBitmapCachesByBPP Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings6
- Interfaz IMsRdpClientAdvancedSettings6 Servicios de Escritorio remoto , propiedad ScaleBitmapCachesByBPP
- Propiedad ScaleBitmapCachesByBPP Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings7
- Interfaz IMsRdpClientAdvancedSettings7 Servicios de Escritorio remoto , propiedad ScaleBitmapCachesByBPP
- Propiedad ScaleBitmapCachesByBPP Servicios de Escritorio remoto , interfaz IMsRdpClientAdvancedSettings8
- Interfaz IMsRdpClientAdvancedSettings8 Servicios de Escritorio remoto , propiedad ScaleBitmapCachesByBPP
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings2.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings2.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings2.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings3.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings3.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings3.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings4.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings4.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings4.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings5.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings5.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings5.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings6.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings6.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings6.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings7.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings7.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings7.put_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings8.ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings8.get_ScaleBitmapCachesByBPP
- IMsRdpClientAdvancedSettings8.put_ScaleBitmapCachesByBPP
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5774a73944bee0a7538c226c5ad6ecd743b5c891a795a6b5201d6fde054ab33
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117941750"
---
# <a name="imsrdpclientadvancedsettingsscalebitmapcachesbybpp-property"></a>Propiedad IMsRdpClientAdvancedSettings::ScaleBitmapCachesByBPP

Esta propiedad no es compatible.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Syntax


```C++
HRESULT put_ScaleBitmapCachesByBPP(
  [in]  LONG bScale
);

HRESULT get_ScaleBitmapCachesByBPP(
  [out] LONG *pbScale
);
```



## <a name="property-value"></a>Valor de propiedad

Establezca este parámetro en 0 para deshabilitar la característica o un valor distinto de cero para habilitar la característica.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ FALSE.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                       |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                       |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>          |
| IID<br/>                      | IID \_ IMsRdpClientAdvancedSettings se define como 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings3**](imstscadvancedsettings-interface.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





