---
title: Método EnrollMethod de la MDM_ClientCertificateInstall_Install03 clase
description: Desencadena el dispositivo para iniciar la inscripción de certificados.
ms.assetid: 21a31574-0b19-44bf-90db-4bb9e2611364
keywords:
- Método EnrollMethod
- Método EnrollMethod, MDM_ClientCertificateInstall_Install03 clase
- MDM_ClientCertificateInstall_Install03 clase, método EnrollMethod
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
ms.openlocfilehash: 1ddeca621f58015aa3806212c1250aeb43554a51cbb28e15414e779571b9c102
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109414"
---
# <a name="enrollmethod-method-of-the-mdm_clientcertificateinstall_install03-class"></a>Método EnrollMethod de la \_ clase MDM ClientCertificateInstall \_ Install03

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Desencadena el dispositivo para iniciar la inscripción de certificados. El dispositivo no notificará al servidor MDM después de que se haya realizado la inscripción de certificados. El servidor MDM podría consultar más adelante el dispositivo para averiguar si se agrega un nuevo certificado. Consulte también [**Inscribir**](/windows/client-management/mdm/clientcertificateinstall-csp).

## <a name="syntax"></a>Sintaxis


```mof
uint32 EnrollMethod();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Obligatorio. Desencadena el dispositivo para iniciar la inscripción de certificados. El dispositivo no notificará al servidor MDM después de que se haya realizado la inscripción de certificados. El servidor MDM podría consultar más adelante el dispositivo para averiguar si se agrega un nuevo certificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 10 solo aplicaciones de escritorio\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                      |
| Espacio de nombres<br/>                | Root \\ cimv2 \\ mdm \\ dmmap<br/>                                                             |
| MOF<br/>                      | <dl> <dt>DMWmiBridgeProv.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>DMWmiBridgeProv.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MDM \_ ClientCertificateInstall \_ Install03**](mdm-clientcertificateinstall-install03.md)
</dt> <dt>

[Uso de scripts de PowerShell con el proveedor de puente WMI](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

