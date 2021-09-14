---
title: Método DeleteEx de la Win32_SessionBrokerFarmAccount clase
description: La clase SessionBrokerFarmAccount de Win32 ya no está disponible para su uso \_ a Windows Server 2012. | Método DeleteEx de la Win32_SessionBrokerFarmAccount clase
ms.assetid: d30c5d3e-f63c-4b21-85ae-a0b8d5868d64
ms.tgt_platform: multiple
keywords:
- Método DeleteEx Servicios de Escritorio remoto
- Método DeleteEx Servicios de Escritorio remoto , Win32_SessionBrokerFarmAccount clase
- Win32_SessionBrokerFarmAccount clase Servicios de Escritorio remoto , método DeleteEx
topic_type:
- apiref
api_name:
- Win32_SessionBrokerFarmAccount.DeleteEx
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdad7b1c7af85337ace59690bb44f4309254eb76
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126891228"
---
# <a name="deleteex-method-of-the-win32_sessionbrokerfarmaccount-class"></a>Método DeleteEx de la clase \_ SessionBrokerFarmAccount de Win32

\[La [**clase \_ SessionBrokerFarmAccount de Win32**](win32-sessionbrokerfarmaccount.md) ya no está disponible para su uso a Windows Server 2012.\]

Elimina la cuenta de granja.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DeleteEx(
  [in] boolean DeleteComputerObject
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DeleteComputerObject* \[ En\]
</dt> <dd>

Indica si el objeto de equipo asociado a la granja se va a quitar de Active Directory.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi. Consulte los [Servicios de Escritorio remoto de error del proveedor WMI](terminal-services-wmi-provider-error-codes.md) para obtener una lista de estos valores.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                      |
| Fin de compatibilidad de cliente<br/>    | No se admite ninguno<br/>                                                              |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2008 R2<br/>                                                      |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**\_SessionBrokerFarmAccount de Win32**](win32-sessionbrokerfarmaccount.md)
</dt> </dl>

 

 





