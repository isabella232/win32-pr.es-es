---
title: Método GetInt32Property de la clase Win32_RDSHServer (Microsoft.diagnostics.appanalysis.h)
description: Recupera un valor de propiedad entero de un objeto \_ RDSHServer de Win32.
ms.assetid: 4601e9cb-927b-4af8-a12b-09a8ca44c2f7
ms.tgt_platform: multiple
keywords:
- Método GetInt32Property Servicios de Escritorio remoto
- Método GetInt32Property Servicios de Escritorio remoto , Win32_RDSHServer clase
- Win32_RDSHServer clase Servicios de Escritorio remoto , Método GetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a2427cfa19a84a8b8988cceacf3e0b836a031f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968488"
---
# <a name="getint32property-method-of-the-win32_rdshserver-class"></a>Método GetInt32Property de la clase \_ RDSHServer de Win32

Recupera un valor de propiedad entero de un [**objeto \_ RDSHServer de Win32.**](win32-rdshserver.md)

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Clave* \[ En\]
</dt> <dd>

Clave que identifica la propiedad que se debe recuperar.

</dd> <dt>

*Valor* \[ out\]
</dt> <dd>

Recibe el valor de propiedad recuperado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error wmi.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                                 |
| Espacio de nombres<br/>                | Rdms \\ de CIMv2 \\ raíz<br/>                                                                                   |
| Encabezado<br/>                   | <dl> <dt>Microsoft.diagnostics.appanalysis.h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl>                    |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**RdsHServer de Win32 \_**](win32-rdshserver.md)
</dt> </dl>

 

 





