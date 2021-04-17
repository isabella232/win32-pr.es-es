---
description: Comprueba si el elemento físico al que se hace referencia puede estar contenido o insertado en el paquete físico.
ms.assetid: 406aaa75-b48c-4377-adb5-e900676b6e36
ms.tgt_platform: multiple
title: Método IsCompatible de la clase CIM_PhysicalPackage
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalPackage.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1957b8d0c1929ff6f7b4ef8c69fa55ea4ccc83b9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659502"
---
# <a name="iscompatible-method-of-the-cim_physicalpackage-class"></a>Método IsCompatible de la \_ clase PhysicalPackage de CIM

El método **IsCompatible** comprueba si el paquete físico al que se hace referencia puede estar contenido o insertado en el paquete físico. En una subclase, el conjunto de códigos de retorno posibles se puede especificar mediante un calificador **ValueMap** en el método. Las cadenas a las que se traduce el contenido **ValueMap** también se pueden especificar en la subclase como calificador de matriz **Values** .

> [!IMPORTANT]
> Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI. WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa la sintaxis de Managed Object Format (MOF). Para obtener más información sobre el uso de este método, consulte [llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ElementToCheck* \[ de\]
</dt> <dd>

Referencia al elemento físico en el que se ejecuta el método **IsCompatible** .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se realiza correctamente y cualquier otro número para indicar un error.

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

[**\_PHYSICALPACKAGE CIM**](iscompatible-method-in-class-cim-physicalpackage.md)
</dt> <dt>

[**\_PHYSICALPACKAGE CIM**](cim-physicalpackage.md)
</dt> </dl>

 

