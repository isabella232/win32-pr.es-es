---
description: Detiene el servicio representado por el objeto derivado de CIM \_ BootService.
ms.assetid: 443a2afa-ed46-4378-a06f-5f9f94af51c9
ms.tgt_platform: multiple
title: Método StopService de la CIM_BootService (Sdoias.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService.StopService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c054a9d05410ddbe7ee7d11c5bd4adba9e0ce83b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062584"
---
# <a name="stopservice-method-of-the-cim_bootservice-class"></a>Método StopService de la clase \_ BootService de CIM

El **método StopService** detiene el servicio representado por el objeto derivado de [**CIM \_ BootService**](cim-bootservice.md). Este método se hereda del [**servicio CIM. \_**](cim-service.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
Integer StopService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

## <a name="remarks"></a>Observaciones

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| Encabezado<br/>                   | <dl> <dt>Sdoias.h</dt> </dl>     |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[CIM \_ BootService](stopservice-method-in-class-cim-bootservice.md)
</dt> <dt>

[**CIM \_ BootService**](cim-bootservice.md)
</dt> </dl>

 

