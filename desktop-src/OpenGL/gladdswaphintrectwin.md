---
title: Función glAddSwapHintRectWIN (Gl.h)
description: La función de devolución de llamada glAddSwapHintRectWIN especifica un conjunto de rectángulos que swapBuffers va a copiar.
ms.assetid: f242e755-8e8a-471a-9884-47efa22a3de6
keywords:
- Función GlAddSwapHintRectWIN OpenGL
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
ms.openlocfilehash: 75077ac2a93e3e952ae3c3daca3ea847f7b4b0efc340da0e980b1a4bec6efa64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118618061"
---
# <a name="gladdswaphintrectwin-function"></a>Función glAddSwapHintRectWIN

La función de devolución de llamada **glAddSwapHintRectWIN** especifica un conjunto de rectángulos que [**swapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers)va a copiar.

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

Coordenada *x*(en coordenadas de ventana) de la esquina inferior izquierda del rectángulo de la región de la sugerencia.

</dd> <dt>

*y* 
</dt> <dd>

*Coordenada y*(en coordenadas de ventana) de la esquina inferior izquierda del rectángulo de la región de la sugerencia.

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

La **función glAddSwapHintRectWIN** acelera la animación al reducir la cantidad de volver a dibujar entre fotogramas. Con **glAddSwapHintRectWIN,** se especifica un conjunto de áreas rectangulares que desea copiar al llamar a [**SwapBuffers**](/windows/desktop/api/wingdi/nf-wingdi-swapbuffers). Cuando no se especifica ningún rectángulo con **glAddSwapHintRectWIN** antes de llamar a **SwapBuffers,** se intercambia todo el búfer de fotogramas. El uso de **glAddSwapHintRectWIN para** copiar solo partes modificadas del búfer puede aumentar significativamente el rendimiento de **SwapBuffers,** especialmente cuando **SwapBuffers** se implementa en software.

La **función glAddSwapHintRectWIN** agrega un rectángulo a la región de sugerencia. Cuando se establece la marca PFD SWAP COPY de la estructura de formato de \_ \_ [**píxelES PIXELFORMATDESCRIPTOR,**](/windows/win32/api/wingdi/ns-wingdi-pixelformatdescriptor) **SwapBuffers** usa esta región para recortar la copia del búfer de reserva en el búfer frontal. No se especifica PFD \_ SWAP \_ COPY; se establece mediante hardware compatible. La región de sugerencia se borra después de cada llamada **a SwapBuffers.** Con algunas configuraciones de hardware, **SwapBuffers** puede omitir la región de sugerencia e intercambiar todo el búfer. **SwapBuffers** lo implementa el sistema, no la aplicación.

OpenGL mantiene una región de sugerencias independiente para cada ventana. Cuando se llama a **glAddSwapHintRectWIN** en cualquier contexto de representación asociado a una ventana, los rectángulos de sugerencia se combinan en una sola región.

Llame **a glAddSwapHintRectWIN** con un rectángulo delimitador para cada objeto dibujado para un marco y para cada rectángulo borrado para borrar los objetos de marco anteriores.

> [!Note]  
> La **función glAddSwapHintRectWIN** es una función de extensión que no forma parte de la biblioteca OpenGL estándar, pero forma parte de la extensión de sugerencia de intercambio \_ DE GL \_ \_ WIN. Para comprobar si la implementación de OpenGL admite **glAddSwapHintRectWIN,** llame **a glGetString**(GL \_ EXTENSIONS). Si devuelve la sugerencia de \_ intercambio GL \_ \_ WIN, se admite **glAddSwapHintRectWIN.** Para obtener la dirección de una función de extensión, llame **a wglGetProcAddress**.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                      |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                            |
| Encabezado<br/>                   | <dl> <dt>Gl.h</dt> </dl> |



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

 

 





