---
description: 'Método StartService de la CIM_Service clase (proveedores WMI CIMWin32): el método StartService coloca el servicio en estado iniciado.'
ms.assetid: 0f2880ed-1643-4211-8684-12493711b1f8
ms.tgt_platform: multiple
title: Método StartService de la clase CIM_Service (proveedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Service.StartService
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 87fcdad650ea93461850bab3e3e66d9543025a2b468b9f7948f6d949d5838c4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119752445"
---
# <a name="startservice-method-of-the-cim_service-class-cimwin32-wmi-providers"></a>Método StartService de la clase CIM_Service (proveedores WMI CIMWin32)

El **método StartService** coloca el servicio en estado iniciado.

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DE DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de la versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis de MOF. Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 StartService();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 (cero) si se ejecuta correctamente y cualquier otro número para indicar un error. En una subclase, el conjunto de códigos de retorno posibles se puede especificar mediante un **calificador ValueMap** en el método . Las cadenas a las que se traduce el contenido **de ValueMap** también se pueden especificar en la subclase como calificador de **matriz Values.**

## <a name="remarks"></a>Comentarios

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



## <a name="see-also"></a>Vea también

<dl> <dt>

[Servicio \_ CIM](startservice-method-in-class-cim-service.md)
</dt> <dt>

[**Servicio \_ CIM**](cim-service.md)
</dt> </dl>

 

