---
title: Método EnrollMethod de la clase MDM_ClientCertificateInstall_Install03
description: Desencadena el dispositivo para iniciar la inscripción de certificados.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Método EnrollMethod
- Método EnrollMethod, clase MDM_ClientCertificateInstall_Install03
- Clase MDM_ClientCertificateInstall_Install03, método EnrollMethod
topic_type:
- apiref
api_name:
- MDM_ClientCertificateInstall_Install03.EnrollMethod
api_location:
- DMWmiBridgeProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7903407d5a97f056835e529eb21408bdcbe800ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803128"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a>Método EnrollMethod de la \_ \_ clase INSTALL03 de MDM ClientCertificateInstall

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Desencadena el dispositivo para iniciar la inscripción de certificados. El dispositivo no notificará al servidor MDM una vez que se haya realizado la inscripción de certificados. El servidor MDM podría consultar posteriormente el dispositivo para averiguar si se ha agregado el nuevo certificado. Vea también [**inscribir**](/windows/client-management/mdm/clientcertificateinstall-csp).

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Obligatorio. Desencadena el dispositivo para iniciar la inscripción de certificados. El dispositivo no notificará al servidor MDM una vez que se haya realizado la inscripción de certificados. El servidor MDM podría consultar posteriormente el dispositivo para averiguar si se ha agregado el nuevo certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Dmmap de MDM raíz de \\ cimv2 \\ \\<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_Install03 CLIENTCERTIFICATEINSTALL \_ MDM**](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[Usar scripting de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

