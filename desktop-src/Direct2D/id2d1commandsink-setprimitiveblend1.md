---
title: Método ID2D1CommandSink1 SetPrimitiveBlend1
description: Establece un nuevo modo de combinación primitivo.
ms.assetid: 3EA9EC07-1B2F-48A2-ABFB-2DA0E2EFFBF4
keywords:
- Método SetPrimitiveBlend1 Direct2D
- Método SetPrimitiveBlend1 Direct2D, interfaz ID2D1CommandSink1
- Interfaz ID2D1CommandSink1 Direct2D, método SetPrimitiveBlend1
topic_type:
- apiref
api_name:
- ID2D1CommandSink1.SetPrimitiveBlend1
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3aa961eec873cc84e5b34ce41279c09f580e63d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127163102"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a>Método ID2D1CommandSink1::SetPrimitiveBlend1

Establece un nuevo modo de combinación primitivo.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetPrimitiveBlend1(
   D2D1_PRIMITIVE_BLEND primitiveBlend
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*primitiveBlend* 
</dt> <dd>

Tipo: **[ **D2D1 \_ PRIMITIVE \_ BLEND**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**

Combinación primitiva que se aplicará a las primitivas posteriores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si el método se realiza correctamente, devuelve **S \_ OK**. Si se produce un error, devuelve un código de error **HRESULT.**

## <a name="remarks"></a>Observaciones

### <a name="blend-modes"></a>Modos de fusión

Para la representación con alias (excepto para el modo MIN), el valor de salida O se calcula interpolando linealmente el valor *blend(S, D)* con el valor de píxel de destino, en función de la cantidad que la primitiva cubre el píxel de destino.

En la tabla siguiente se muestran los modos de combinación primitivos para la combinación con alias y suavizado de contorno. Las ecuaciones enumeradas en la tabla usan estos elementos:

-   O = Salida
-   S = Origen
-   SA = Alfa de origen
-   D = Destino
-   DA = Alfa de destino
-   C = Cobertura de píxeles



| Modo de combinación primitivo                 | Combinación con alias                            | Combinación con suavizado de contorno            | Descripción                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ PRIMITIVE \_ BLEND \_ SOURCE \_ OVER | O = (S + (1 SA) \* D) \* C + D \* (1 C) | O = S \* C + D \* (1 SA \* C)   | Modo blend de origen sobre destino estándar.                                                                         |
| COPIA DE BLEND PRIMITIVA D2D1 \_ \_ \_         | O = S \* C + D \* (1 C)                   | O = S \* C + D \* (1 C)       | El origen se copia en el destino; se omiten los píxeles de destino.                                             |
| D2D1 \_ PRIMITIVE \_ BLEND \_ MIN          | O = Min(S + 1-SA, D)                        | O = Min(S \* C + 1 SA \* C, D) | Los valores de píxel resultantes usan el mínimo de los valores de píxel de origen y destino. Disponible en Windows 8 y versiones posteriores. |
| D2D1 \_ PRIMITIVE \_ BLEND \_ ADD          | O = (S + D) \* C + D \* (1 C)             | O = S \* C + D                  | Los valores de píxel resultantes son la suma de los valores de píxel de origen y destino. Disponible en Windows 8 y versiones posteriores.     |



 

![ilustración de los modos de combinación primitivos de Direct2d con opacidad y fondos variables.](images/primblenddemo.png)

Ilustración de los modos de combinación primitivos con opacidad y fondos variables.

La combinación primitiva se aplicará a todas las primitivas dibujadas en el contexto, a menos que se invalide con el *parámetro compositeMode* en la API [**DrawImage.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode))

La combinación primitiva se aplica al interior de cualquier primitivo dibujado en el contexto. En el caso de [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), esto estará implícito en el rectángulo de la imagen, el desplazamiento y la transformación del mundo.

Si la combinación primitiva es cualquier cosa que no **sea D2D1 \_ PRIMITIVE BLEND \_ \_ OVER,** se desactivará la representación de ClearType. Si la aplicación fuerza explícitamente la representación de ClearType en estos modos, el contexto de dibujo se colocará en un estado de error. D2DERR \_ WRONG STATE se devolverá desde \_ [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 aplicaciones de escritorio \| aplicaciones para UWP\]<br/>                                     |
| Servidor mínimo compatible<br/> | Windows Server 2012 Aplicaciones de \[ escritorio R2 \| aplicaciones para UWP\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 y Windows Runtime\]<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ID2D1CommandSink1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

