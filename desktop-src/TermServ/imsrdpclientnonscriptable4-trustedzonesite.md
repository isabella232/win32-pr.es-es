---
title: Propiedad TrustedZoneSite de IMsRdpClientNonScriptable4
description: Especifica si el sitio web desde el que el usuario inició la conexión se encuentra en la lista de sitios de confianza del equipo cliente del usuario.
ms.assetid: cb7efacc-b13b-494c-ab02-35c4f914744c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad TrustedZoneSite
- Propiedad TrustedZoneSite Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad TrustedZoneSite
- Propiedad TrustedZoneSite Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad TrustedZoneSite
- Servicios de Escritorio remoto de la propiedad TrustedZoneSite, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad TrustedZoneSite
- Servicios de Escritorio remoto de la propiedad TrustedZoneSite, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad TrustedZoneSite
- Servicios de Escritorio remoto de la propiedad TrustedZoneSite, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad TrustedZoneSite
- Servicios de Escritorio remoto de la propiedad TrustedZoneSite, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad TrustedZoneSite
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.TrustedZoneSite
- IMsRdpClientNonScriptable4.get_TrustedZoneSite
- IMsRdpClientNonScriptable4.put_TrustedZoneSite
- IMsRdpClientNonScriptable5.TrustedZoneSite
- IMsRdpClientNonScriptable5.get_TrustedZoneSite
- IMsRdpClientNonScriptable5.put_TrustedZoneSite
- MsRdpClient6.TrustedZoneSite
- MsRdpClient7.TrustedZoneSite
- MsRdpClient8.TrustedZoneSite
- MsRdpClient9.TrustedZoneSite
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791b5eff3346f61f999ea1f4f78bc41a5acea0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422430"
---
# <a name="imsrdpclientnonscriptable4trustedzonesite-property"></a>IMsRdpClientNonScriptable4:: TrustedZoneSite (propiedad)

Especifica si el sitio web desde el que el usuario inició la conexión se encuentra en la lista de sitios de confianza del equipo cliente del usuario.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_TrustedZoneSite(
  [in]  VARIANT_BOOL fIsTrustedZone
);

HRESULT get_TrustedZoneSite(
  [out] VARIANT_BOOL *pfIsTrustedZone
);
```



## <a name="property-value"></a>Valor de propiedad

Establece la propiedad TrustedZoneSite. Este método no tiene ningún efecto sobre si el sitio web desde el que el usuario inició la conexión se encuentra en la lista de sitios de confianza del equipo cliente.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IMsRdpClientNonScriptable4 se define como f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





