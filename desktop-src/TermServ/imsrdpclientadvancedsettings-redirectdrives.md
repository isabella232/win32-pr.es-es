---
title: Propiedad RedirectDrives de IMsRdpClientAdvancedSettings
description: Especifica si se permite la redirección de unidades de disco.
ms.assetid: 5ed4cd28-4a1f-4d3b-9f9d-bf44a8483209
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings2
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings2, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings3, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings4, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings6
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings6, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, propiedad RedirectDrives
- Propiedad RedirectDrives Servicios de Escritorio remoto, interfaz IMsRdpClientAdvancedSettings8
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings8, propiedad RedirectDrives
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RedirectDrives
- IMsRdpClientAdvancedSettings.get_RedirectDrives
- IMsRdpClientAdvancedSettings.put_RedirectDrives
- IMsRdpClientAdvancedSettings2.RedirectDrives
- IMsRdpClientAdvancedSettings2.get_RedirectDrives
- IMsRdpClientAdvancedSettings2.put_RedirectDrives
- IMsRdpClientAdvancedSettings3.RedirectDrives
- IMsRdpClientAdvancedSettings3.get_RedirectDrives
- IMsRdpClientAdvancedSettings3.put_RedirectDrives
- IMsRdpClientAdvancedSettings4.RedirectDrives
- IMsRdpClientAdvancedSettings4.get_RedirectDrives
- IMsRdpClientAdvancedSettings4.put_RedirectDrives
- IMsRdpClientAdvancedSettings5.RedirectDrives
- IMsRdpClientAdvancedSettings5.get_RedirectDrives
- IMsRdpClientAdvancedSettings5.put_RedirectDrives
- IMsRdpClientAdvancedSettings6.RedirectDrives
- IMsRdpClientAdvancedSettings6.get_RedirectDrives
- IMsRdpClientAdvancedSettings6.put_RedirectDrives
- IMsRdpClientAdvancedSettings7.RedirectDrives
- IMsRdpClientAdvancedSettings7.get_RedirectDrives
- IMsRdpClientAdvancedSettings7.put_RedirectDrives
- IMsRdpClientAdvancedSettings8.RedirectDrives
- IMsRdpClientAdvancedSettings8.get_RedirectDrives
- IMsRdpClientAdvancedSettings8.put_RedirectDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c83d24ae4ea4dae2760c1e468f4fa8b326a94c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803890"
---
# <a name="imsrdpclientadvancedsettingsredirectdrives-property"></a>IMsRdpClientAdvancedSettings:: RedirectDrives (propiedad)

Especifica si se permite la redirección de unidades de disco.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_RedirectDrives(
  [in]  VARIANT_BOOL redirectDrives
);

HRESULT get_RedirectDrives(
  [out] VARIANT_BOOL *predirectDrives
);
```



## <a name="property-value"></a>Valor de propiedad

Establezca este parámetro en **Variant \_ true** para permitir el redireccionamiento o **Variant \_ false** en caso contrario. **Variante \_ TRUE** solicita al usuario que confirme que permite la redirección en el tiempo de conexión, por motivos de seguridad.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="remarks"></a>Observaciones

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                        |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                  |
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

 

 





