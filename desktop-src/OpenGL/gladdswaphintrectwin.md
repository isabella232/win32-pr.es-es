---
title: función glAddSwapHintRectWIN (GL. h)
description: La función de devolución de llamada glAddSwapHintRectWIN especifica un conjunto de rectángulos que se van a copiar mediante SwapBuffers.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- glAddSwapHintRectWIN (función) OpenGL
topic_type:
- apiref
api_name:
- glAddSwapHintRectWIN
api_location:
- Gl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae3e10c2f51ff8d7c9763ff1dad7d09d800cd60
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422400"
---
# <a name="gladdswaphintrectwin-function"></a>glAddSwapHintRectWIN función)

La función de devolución de llamada **glAddSwapHintRectWIN** especifica un conjunto de rectángulos que se van a copiar mediante [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers).

## <a name="syntax"></a>Sintaxis


```C++
void WINAPI glAddSwapHintRectWIN(
   GLint   x,
   GLint   y,
   GLsizei width,
   GLsizei height
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*x* 
</dt> <dd>

La coordenada *x*(en coordenadas de la ventana) de la esquina inferior izquierda del rectángulo de la región de sugerencia.

</dd> <dt>

*y* 
</dt> <dd>

Coordenada *y*(en coordenadas de la ventana) de la esquina inferior izquierda del rectángulo de la región de sugerencia.

</dd> <dt>

*width* 
</dt> <dd>

Ancho del rectángulo de la región de la sugerencia.

</dd> <dt>

*height* 
</dt> <dd>

Alto del rectángulo de la región de la sugerencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

La función **glAddSwapHintRectWIN** acelera la animación reduciendo la cantidad de repintado entre fotogramas. Con **glAddSwapHintRectWIN**, debe especificar un conjunto de áreas rectangulares que desea copiar al llamar a [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). Cuando no se especifica ningún rectángulo con **glAddSwapHintRectWIN** antes de llamar a **SwapBuffers**, se intercambia todo el fotogramas. El uso de **glAddSwapHintRectWIN** para copiar solo las partes modificadas del búfer puede aumentar significativamente el rendimiento de **SwapBuffers**, especialmente cuando se implementa **SwapBuffers** en el software.

La función **glAddSwapHintRectWIN** agrega un rectángulo a la región de sugerencia. Cuando \_ \_ se establece la marca de copia de intercambio de PFD de la estructura de formato de píxel de [**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) , **SwapBuffers** usa esta región para recortar la copia del búfer de reserva en el búfer frontal. No se especifica la \_ \_ copia de intercambio de PFD; está establecida por hardware compatible. La región de sugerencia se borra después de cada llamada a **SwapBuffers**. Con algunas configuraciones de hardware, **SwapBuffers** puede omitir la región de sugerencia e intercambiar todo el búfer. **SwapBuffers** se implementa mediante el sistema, no por la aplicación.

OpenGL mantiene una región de sugerencia independiente para cada ventana. Cuando se llama a **glAddSwapHintRectWIN** en todos los contextos de representación asociados a una ventana, los rectángulos de la sugerencia se combinan en una sola región.

Llame a **glAddSwapHintRectWIN** con un rectángulo delimitador para cada objeto dibujado para un marco y para cada rectángulo desactivado para borrar los objetos de fotogramas anteriores.

> [!Note]  
> La función **glAddSwapHintRectWIN** es una función de extensión que no forma parte de la biblioteca estándar de OpenGL, pero que forma parte de la extensión de sugerencia de intercambio de cont \_ \_ \_ . Para comprobar si la implementación de OpenGL es compatible con **glAddSwapHintRectWIN**, llame a **glGetString**(extensiones de GL \_ ). Si devuelve la \_ sugerencia GL Win \_ swap \_ , se admite **glAddSwapHintRectWIN** . Para obtener la dirección de una función de extensión, llame a **wglGetProcAddress**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                            |
| Encabezado<br/>                   | <dl> <dt>GL. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**glGetString**](glgetstring.md)
</dt> <dt>

[**PIXELFORMATDESCRIPTOR**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor)
</dt> <dt>

[**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)
</dt> <dt>

[**wglGetProcAddress**](/windows/desktop/api/wingdi/nf-wingdi-wglgetprocaddress)
</dt> </dl>

 

 





