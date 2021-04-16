---
description: La función de exportación FormatProperties da formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de Monitor de red. Si desea mostrar los datos en el panel de detalles, debe implementar la función de exportación FormatProperties en todos los archivos dll de analizador.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Función de devolución de llamada FormatProperties (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 61707b49fa88490e1aa22ac89f33dfd97ec20cbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666287"
---
# <a name="formatproperties-callback-function"></a>Función de devolución de llamada FormatProperties

La función de exportación **FormatProperties** da formato a los datos que se muestran en el panel de detalles de la interfaz de usuario de monitor de red. Si desea mostrar los datos en el panel de detalles, debe implementar la función de exportación **FormatProperties** en todos los archivos dll de analizador.

## <a name="syntax"></a>Sintaxis


```C++
DWORD FormatProperties(
  _In_ HFRAME         hFrame,
  _In_ LPBYTE         lpFrame,
  _In_ LPBYTE         lpProtocol,
  _In_ DWORD          nPropertyInsts,
  _In_ LPPROPERTYINST lpPropInst
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ de\]
</dt> <dd>

Identificador del marco que se está analizando.

</dd> <dt>

*lpFrame* \[ de\]
</dt> <dd>

Puntero al primer byte de un marco.

</dd> <dt>

*lpProtocol* \[ de\]
</dt> <dd>

Puntero al principio de los datos de protocolo en un marco.

</dd> <dt>

*nPropertyInsts* \[ de\]
</dt> <dd>

Número de estructuras [PROPERTYINST](propertyinst.md) proporcionadas por *lpPropInst*.

</dd> <dt>

*lpPropInst* \[ de\]
</dt> <dd>

Puntero a una matriz de estructuras [PROPERTYINST](propertyinst.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **true**.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

Monitor de red llama a la función **FormatProperties** para mostrar los datos en el panel de detalles de la interfaz de usuario de monitor de red. Normalmente, se llama a **FormatProperties** para dar formato a la línea de Resumen de un protocolo y, a continuación, para dar formato a todas las instancias de propiedad del protocolo dentro de un marco. Sin embargo, Monitor de red no garantiza el número de veces que llama a **FormatProperties** para un analizador específico.

Durante la implementación de la función **FormatProperties** , el analizador llama indirectamente a la función [FormatPropertyInstance](formatpropertyinstance.md) para usar el formateador genérico que proporciona monitor de red, o puede llamar a un procedimiento de formateador personalizado definido por el analizador. Se debe llamar a uno de los formateadores para cada estructura [PROPERTYINST](propertyinst.md) pasada a la dll del analizador en el parámetro *lpPropInst* .



| Para obtener información sobre                                          | Vea                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red.   | [Analizadores](parsers.md)                                             |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.          | [Arquitectura de DLL de analizador](parser-dll-architecture.md)             |
| Cómo implementar **FormatProperties**  incluye un ejemplo. | [Implementación de FormatProperties](implementing-formatproperties.md) |
| Cómo el formateador genérico da formato a distintos tipos de datos.  | [Salida del formateador genérico](generic-formatter-output.md)           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[FormatPropertyInstance](formatpropertyinstance.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




