---
title: Mensaje de LB_SETTABSTOPS (Winuser. h)
description: Establece las posiciones de tabulación en un cuadro de lista.
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- LB_SETTABSTOPS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21927aaf82624242e8d42ef4a7459f1e36cdf74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905510"
---
# <a name="lb_settabstops-message"></a>\_Mensaje lb SETTABSTOPS

Establece las posiciones de tabulación en un cuadro de lista.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica el número de tabulaciones.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero al primer miembro de una matriz de enteros que contiene las tabulaciones. Los enteros representan el número de cuartos del ancho promedio de caracteres de la fuente seleccionada en el cuadro de lista. Por ejemplo, una tabulación de 4 se coloca en unidades de 1,0 caracteres y una posición de tabulación de 6 se coloca en las unidades de caracteres de promedio de 1,5. Sin embargo, si el cuadro de lista forma parte de un cuadro de diálogo, los enteros se encuentran en unidades de plantilla de cuadro de diálogo. Las tabulaciones se deben ordenar en orden ascendente; no se permiten pestañas hacia atrás.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si se establecen todas las pestañas especificadas, el valor devuelto es **true**; de lo contrario, es **false**.

## <a name="remarks"></a>Observaciones

Para responder al mensaje de **lb \_ SETTABSTOPS** , el cuadro de lista se debe haber creado con el estilo [**lbs \_ USETABSTOPS**](list-box-styles.md) .

Si *wParam* es 0 y *lParam* es **null**, la tabulación predeterminada es dos unidades de plantilla de cuadro de diálogo. Si *wParam* es 1, el cuadro de lista tendrá posiciones de tabulación separadas por la distancia especificada por *lParam*.

Si *lParam* apunta a más de un valor, se establecerá una detención de tabulación para cada valor de *lParam*, hasta el número especificado por *wParam*.

Los valores especificados por *lParam* están en unidades de plantilla de cuadro de diálogo, que son las unidades independientes del dispositivo que se usan en las plantillas de cuadro de diálogo. Para convertir las medidas de las unidades de plantilla de cuadro de diálogo en unidades de pantalla (píxeles), use la función [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .

Windows 95, Windows 98 o Windows Millennium Edition (Windows me): el búfer señalado por *lParam* debe residir en la memoria de escritura, aunque el mensaje no modifique la matriz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

