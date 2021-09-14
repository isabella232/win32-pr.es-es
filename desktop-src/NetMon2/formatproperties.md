---
description: La función de exportación FormatProperties da formato a los datos que se muestran en el panel de detalles de la interfaz Monitor de red usuario. Si desea mostrar datos en el panel de detalles, debe implementar la función de exportación FormatProperties en todos los archivos DLL del analizador.
ms.assetid: 78e0b4b9-f19e-41cb-8504-635f3f9ac1ee
title: Función de devolución de llamada FormatProperties (Netmon.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074158"
---
# <a name="formatproperties-callback-function"></a>Función de devolución de llamada FormatProperties

La función de exportación **FormatProperties** da formato a los datos que se muestran en el panel de detalles de la interfaz Monitor de red usuario. Si desea mostrar datos en el panel de detalles, debe implementar la función de exportación **FormatProperties** en todos los archivos DLL del analizador.

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

*hFrame* \[ En\]
</dt> <dd>

Controle el marco que se está analizando.

</dd> <dt>

*lpFrame* \[ En\]
</dt> <dd>

Puntero al primer byte de un marco.

</dd> <dt>

*lpProtocol* \[ En\]
</dt> <dd>

Puntero al principio de los datos del protocolo en un marco.

</dd> <dt>

*nPropertyInsts* \[ En\]
</dt> <dd>

Número de [estructuras PROPERTYINST](propertyinst.md) proporcionadas por *lpPropInst.*

</dd> <dt>

*lpPropInst* \[ En\]
</dt> <dd>

Puntero a una matriz de [estructuras PROPERTYINST.](propertyinst.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **TRUE.**

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Observaciones

Monitor de red llama a **la función FormatProperties** para mostrar datos en el panel de detalles de la interfaz Monitor de red usuario. Normalmente, se llama a **FormatProperties** para dar formato a la línea de resumen de un protocolo y, a continuación, para dar formato a todas las instancias de propiedad del protocolo dentro de un marco. Sin embargo, Monitor de red no garantiza el número de veces que llama a **FormatProperties** para un analizador específico.

Durante la implementación de la función **FormatProperties,** el analizador llama indirectamente a la función [FormatPropertyInstance](formatpropertyinstance.md) para usar el formateador genérico que proporciona Monitor de red o puede llamar a un procedimiento de formateador personalizado definido por el analizador. Se debe llamar a uno de los formateadores para cada estructura [PROPERTYINST](propertyinst.md) pasada al archivo DLL del analizador en el *parámetro lpPropInst.*



| Para obtener información sobre                                          | Vea                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red.   | [Analizadores](parsers.md)                                             |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.          | [Arquitectura dll del analizador](parser-dll-architecture.md)             |
| La implementación de **FormatProperties**  incluye un ejemplo. | [Implementar FormatProperties](implementing-formatproperties.md) |
| Cómo el formateador genérico da formato a diferentes tipos de datos.  | [Salida de formateador genérico](generic-formatter-output.md)           |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[FormatPropertyInstance](formatpropertyinstance.md)
</dt> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




