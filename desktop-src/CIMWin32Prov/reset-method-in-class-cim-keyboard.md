---
description: El método Reset de la \_ clase de teclado CIM solicita un restablecimiento del dispositivo lógico.
ms.assetid: 737bd50c-8e40-4f60-9deb-587b6f37c151
ms.tgt_platform: multiple
title: Método Reset de la clase CIM_Keyboard
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Keyboard.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8e5296953e157182c97e113539b1b47625a0de44
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000685"
---
# <a name="reset-method-of-the-cim_keyboard-class"></a>Método Reset de la \_ clase de teclado CIM

El método **RESET** de la \_ clase de teclado CIM solicita un restablecimiento del dispositivo lógico. Este método se hereda del [**\_ LogicalDevice de CIM**](cim-logicaldevice.md).

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintaxis


```mof
uint32 Reset();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve 0 (cero) si la solicitud se ejecutó correctamente, 1 (uno) si no se admite la solicitud y otro valor si se produjo un error.

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

[\_Teclado CIM](reset-method-in-class-cim-keyboard.md)
</dt> <dt>

[**\_Teclado CIM**](cim-keyboard.md)
</dt> </dl>

 

 




