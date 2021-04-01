---
title: ID2D1CommandSink1 SetPrimitiveBlend1, método
description: Establece un nuevo modo de mezcla primitivo.
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150226"
---
# <a name="id2d1commandsink1setprimitiveblend1-method"></a>ID2D1CommandSink1:: SetPrimitiveBlend1 (método)

Establece un nuevo modo de mezcla primitivo.

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

Tipo: **[ **D2D1 \_ primitiva \_ Blend**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)**

Combinación primitiva que se aplicará a los primitivos posteriores.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HRESULT**

Si el método se ejecuta correctamente, devuelve **S \_ correcto**. Si se produce un error, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

### <a name="blend-modes"></a>Modos de fusión

En la representación con alias (excepto en el modo MIN), el valor de salida O se calcula mediante la interpolación lineal del valor *Blend (S, D)* con el valor de píxel de destino, en función de la cantidad que el primitivo cubre el píxel de destino.

En la tabla siguiente se muestran los modos de mezcla primitivos para la combinación con alias y con suavizado de contorno. Las ecuaciones que aparecen en la tabla usan estos elementos:

-   O = salida
-   S = origen
-   SA = alfa de origen
-   D = destino
-   DA = alfa de destino
-   C = cobertura de píxeles



| Modo de mezcla primitivo                 | Combinación con alias                            | Mezcla suavizada            | Descripción                                                                                                              |
|--------------------------------------|---------------------------------------------|---------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| \_Origen de mezcla primitivo de D2D1 \_ \_ \_ sobre | O = (S + (1 SA) \* D) \* C + D \* (1 C) | O = S \* C + D \* (1 SA \* C)   | Modo de mezcla de origen a destino estándar.                                                                         |
| \_Copia de \_ Blend D2D1 primitiva \_         | O = S \* C + D \* (1 c)                   | O = S \* C + D \* (1 c)       | El origen se copia en el destino; los píxeles de destino se omiten.                                             |
| D2D1 \_ primitiva de \_ mezcla \_ mínima          | O = min (S + 1-SA, D)                        | O = min (S \* c + 1 SA \* C, D) | Los valores de píxeles resultantes usan el mínimo de los valores de píxel de origen y de destino. Disponible en Windows 8 y versiones posteriores. |
| D2D1 \_ primitiva \_ Blend \_ Add          | O = (S + D) \* C + d \* (1 c)             | O = S \* C + D                  | Los valores de píxeles resultantes son la suma de los valores de los píxeles de origen y de destino. Disponible en Windows 8 y versiones posteriores.     |



 

![Ilustración de los modos de mezcla primitivos de direct2d con opacidad y fondo variables.](images/primblenddemo.png)

Ilustración de los modos de mezcla primitivos con opacidad y fondo variables.

La mezcla primitiva se aplicará a toda la primitiva dibujada en el contexto, a menos que se invalide con el parámetro *compositeMode* en la API [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) .

La mezcla primitiva se aplica al interior de cualquier primitiva dibujada en el contexto. En el caso de [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)), lo implicará el rectángulo de imagen, el desplazamiento y la transformación universal.

Si la mezcla primitiva es algo que no sea **D2D1 \_ primitiva \_ Blend \_** , se desactivará la representación de ClearType. Si la aplicación fuerza explícitamente la representación ClearType en estos modos, el contexto de dibujo se colocará en un estado de error. Se \_ \_ devolverá un estado incorrecto de D2DERR desde [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) o [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Aplicaciones \[ para UWP de Windows 8.1 Desktop apps \|\]<br/>                                     |
| Servidor mínimo compatible<br/> | \[Aplicaciones para UWP de aplicaciones de escritorio de Windows Server 2012 R2 \|\]<br/>                          |
| Teléfono mínimo compatible<br/>  | Windows Phone 8,1 \[ Windows Phone aplicaciones de Windows Runtime Silverlight 8,1 y\]<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ID2D1CommandSink1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1commandsink1)
</dt> </dl>

 

