---
description: Comprueba si el bastidor al que se hace referencia se puede contener o insertar en el paquete físico.
ms.assetid: 03276c6a-ca48-48bc-adbe-e53e02107abb
ms.tgt_platform: multiple
title: Método IsCompatible de la CIM_Rack clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6855b797e8941882aac1dc25d77b2ef7e3bc11c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266647"
---
# <a name="iscompatible-method-of-the-cim_rack-class"></a>Método IsCompatible de la clase Cim \_ Rack

El **método IsCompatible** comprueba si el bastidor al que se hace referencia se puede contener o insertar en el paquete físico. En una subclase, el conjunto de códigos de retorno posibles se puede especificar mediante un **calificador ValueMap** en el método . Las cadenas a las que se traduce el contenido **de ValueMap** también se pueden especificar en la subclase como calificador de **matriz Values.** Este método se hereda de [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement ElementToCheck
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ElementToCheck* \[ En\]
</dt> <dd>

Referencia al elemento físico con el que se ejecuta este método.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error.

## <a name="remarks"></a>Observaciones

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Bastidor \_ CIM**](iscompatible-method-in-class-cim-rack.md)
</dt> <dt>

[**Bastidor \_ CIM**](cim-rack.md)
</dt> </dl>

 

