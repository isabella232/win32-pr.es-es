---
title: Propiedad StartProgram de IMsTscSecuredSettings
description: Especifica el programa que se va a iniciar en el servidor remoto en el momento de la conexión.
ms.assetid: bd2a5ced-468b-48db-ad51-9940577a0310
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad StartProgram
- Propiedad StartProgram Servicios de Escritorio remoto, interfaz IMsTscSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsTscSecuredSettings, propiedad StartProgram
- Propiedad StartProgram Servicios de Escritorio remoto, interfaz IMsRdpClientSecuredSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpClientSecuredSettings, propiedad StartProgram
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686210"
---
# <a name="imstscsecuredsettingsstartprogram-property"></a>IMsTscSecuredSettings:: StartProgram (propiedad)

Especifica el programa que se va a iniciar en el servidor remoto en el momento de la conexión.

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

Nombre del nuevo programa de inicio. La longitud máxima de esta cadena es **la \_ ruta de acceso Max**-1 caracteres.

## <a name="error-codes"></a>Códigos de error

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="remarks"></a>Observaciones

Si no se establece el valor de esta propiedad, se ejecutará el comando de Shell del usuario de la sesión. El comando de Shell se leerá desde el siguiente valor del registro en el servidor:

**HKEY \_ SOFTWARE de \_ equipo local** \\  \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Winlogon** \\ **Shell**

Para obtener más información, consulte [proporcionar seguridad de cliente RDP](providing-for-rdp-client-security.md) .

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





