---
description: Comprueba si el chasis físico al que se hace referencia puede contener o insertarse en el paquete físico.
ms.assetid: 9a1aa1b7-2b95-4887-9d14-e416ff69f9df
ms.tgt_platform: multiple
title: Método IsCompatible de la CIM_Chassis clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0bbaa063006d6c7829b3a38b0bc28be78c451b0f2302897a456e1be4cf9eb6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003295"
---
# <a name="iscompatible-method-of-the-cim_chassis-class"></a>Método IsCompatible de la clase \_ Cim Chassis

El **método IsCompatible** comprueba si el chasis físico al que se hace referencia puede contener o insertarse en el paquete físico. En una subclase, el conjunto de códigos de retorno posibles se puede especificar mediante un [**calificador ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) en el método . Las cadenas a las que se traduce el contenido de **ValueMap** también se pueden especificar en la subclase como calificador de **matriz Values.** Este método se hereda de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se construyen las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis MOF (MOF). Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ElementToCheck* \[ En\]
</dt> <dd>

Referencia al elemento físico para el que se va a comprobar la compatibilidad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente, 1 (uno) si no se admite la solicitud y cualquier otro número para indicar un error.

## <a name="remarks"></a>Comentarios

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Chasis \_ CIM**](iscompatible-method-in-class-cim-chassis.md)
</dt> <dt>

[**Chasis \_ CIM**](cim-chassis.md)
</dt> </dl>

 

