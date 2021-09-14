---
title: Propiedad StartProgram de IMsTscSecuredSettings
description: Especifica el programa que se va a iniciar en el servidor remoto tras la conexión.
ms.assetid: bd2a5ced-468b-48db-ad51-9940577a0310
ms.tgt_platform: multiple
keywords:
- Propiedad StartProgram Servicios de Escritorio remoto
- Propiedad StartProgram Servicios de Escritorio remoto interfaz , IMsTscSecuredSettings
- Interfaz IMsTscSecuredSettings Servicios de Escritorio remoto , propiedad StartProgram
- Propiedad StartProgram Servicios de Escritorio remoto interfaz , IMsRdpClientSecuredSettings
- Interfaz IMsRdpClientSecuredSettings Servicios de Escritorio remoto , propiedad StartProgram
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings.StartProgram
- IMsTscSecuredSettings.get_StartProgram
- IMsTscSecuredSettings.put_StartProgram
- IMsRdpClientSecuredSettings.StartProgram
- IMsRdpClientSecuredSettings.get_StartProgram
- IMsRdpClientSecuredSettings.put_StartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e79612855117f48e629e9a06246f3fad922d37f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127168701"
---
# <a name="imstscsecuredsettingsstartprogram-property"></a>Propiedad IMsTscSecuredSettings::StartProgram

Especifica el programa que se va a iniciar en el servidor remoto tras la conexión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_StartProgram(
  [in]  BSTR newVal
);

HRESULT get_StartProgram(
  [out] BSTR *pStartProgram
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre del nuevo programa de inicio. La longitud máxima de esta cadena es **MAX \_ PATH**-1 caracteres.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="remarks"></a>Observaciones

Si no se establece el valor de esta propiedad, se ejecutará el comando shell del usuario de sesión. El comando de shell se leerá del siguiente valor del Registro en el servidor:

**HKEY \_ SOFTWARE DE \_ MÁQUINA** \\ **LOCAL** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **WinLogon** \\ **Shell**

Consulte Proporcionar [seguridad de cliente RDP](providing-for-rdp-client-security.md) para obtener más información.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                 |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>   |
| IID<br/>                      | IID \_ IMsTscSecuredSettings se define como c9d65442-a0f9-45b2-8f73-d61d2db8cbb6<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> <dt>

[**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md)
</dt> </dl>

 

 





