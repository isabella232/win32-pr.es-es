---
description: El método StartService coloca el servicio en un &\# 0034; inicie&\# 0034; State.
ms.assetid: b2b38d64-b497-46f5-8638-a9a8ce50e888
ms.tgt_platform: multiple
title: Método StartService de la clase CIM_BootService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BootService.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e7f7f56633319f9e009f58f7c06dde7a3baee8e5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000827"
---
# <a name="startservice-method-of-the-cim_bootservice-class"></a>Método StartService de la \_ clase BootService de CIM

El método **StartService** pone el servicio en un estado de "Inicio". En una subclase, el conjunto de códigos de retorno posibles se puede especificar mediante un calificador **ValueMap** en el método. Las cadenas a las que se traduce el contenido **ValueMap** también se pueden especificar en la subclase como calificador de matriz **Values** . Este método se hereda del [**\_ servicio CIM**](cim-service.md).

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, vea [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
Integer StartService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

## <a name="remarks"></a>Observaciones

Este método no está implementado actualmente por WMI. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | Origen de \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[\_BOOTSERVICE CIM](startservice-method-in-class-cim-bootservice.md)
</dt> <dt>

[**\_BOOTSERVICE CIM**](cim-bootservice.md)
</dt> </dl>

 

