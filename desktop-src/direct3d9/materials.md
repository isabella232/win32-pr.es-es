---
description: Los materiales describen cómo los polígonos reflejan la luz o parecen emitir luz en una escena 3D.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Materiales (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e8140de30243c7a0f7290715da3d0720cd15cea769bd78cbf66893c0082062d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118092962"
---
# <a name="materials-direct3d-9"></a>Materiales (Direct3D 9)

Los materiales describen cómo los polígonos reflejan la luz o parecen emitir luz en una escena 3D. Las propiedades de material detallan las características de reflexión difusa, reflexión ambiente, emisión de luz y resaltado especular de un material. Direct3D usa la estructura [**D3DMATERIAL9 para**](d3dmaterial9.md) llevar toda la información de propiedades de material. A excepción de la propiedad especular, cada propiedad se describe como un color RGBA que representa la cantidad de partes roja, verde y azul de un tipo determinado de luz que refleja y un factor de mezcla alfa.

## <a name="diffuse-and-ambient-reflection"></a>Reflexión difusa y ambiente

Los miembros Difusos y Ambientales de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) describen cómo un material refleja la luz ambiente y difusa en una escena. Dado que la mayoría de las escenas contienen mucha más luz difusa que la luz ambiente, la reflexión difusa desempeña la mayor parte a la hora de determinar el color. Además, dado que la luz difusa es direccional, el ángulo de la incidencia de la luz difusa afecta a la intensidad general de la reflexión. La reflexión difusa es mayor cuando la luz encuentra un vértice paralelo al vértice normal. A medida que aumenta el ángulo, disminuye el efecto de la reflexión difusa. La cantidad de luz reflejada es el coseno del ángulo entre la luz entrante y el vértice normal, como se muestra en la ilustración siguiente.

![ilustración de la cantidad de luz reflejada](images/incident.png)

La reflexión ambiente, como la luz ambiente, es no bidireccional. La reflexión ambiental tiene un impacto menor en el color aparente de un objeto representado, pero afecta al color general y es más perceptible cuando poca o ninguna luz difusa refleja el material. La reflexión ambiente de un material se ve afectada por el conjunto de luz ambiente de una escena mediante una llamada al método [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con la marca AMBIENT D3DRS. \_

La reflexión difusa y ambiente funcionan conjuntamente para determinar el color percibido de un objeto y suelen ser valores idénticos. Por ejemplo, para representar un objeto azul, se crea un material que refleja solo el componente azul de la luz difusa y ambiental. Cuando se coloca en una sala con una luz blanca, el cristal parece ser azul. Sin embargo, en una sala que solo tiene luz roja, el mismo cristal parecería ser negro, porque su material no refleja la luz roja.

## <a name="emission"></a>Emisión

Los materiales se pueden usar para hacer que un objeto representado parezca autoeconsonado. El miembro emisivo de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) se usa para describir el color y la transparencia de la luz emitida. La emisión afecta al color de un objeto y, por ejemplo, puede hacer que un material oscuro sea más brillante y tomar parte del color emitido.

Puede usar la propiedad emisiva de un material para agregar la sensación de que un objeto emite luz, sin incurrir en la sobrecarga computacional de agregar una luz a la escena. En el caso del azul, la propiedad emissive es útil si desea que el cristal parezca que se enciende, pero no proyecta luz sobre otros objetos de la escena. Recuerde que los materiales con propiedades emisivas no emiten luz que otros objetos de una escena puedan reflejar. Para lograr esta luz reflejada, debe colocar una luz adicional dentro de la escena.

## <a name="specular-reflection"></a>Reflexión especular

La reflexión especular crea resaltados en los objetos, lo que hace que parezcan brillantes. La [**estructura D3DMATERIAL9**](d3dmaterial9.md) contiene dos miembros que describen el color de resaltado especular, así como la disponibilidad general del material. Para establecer el color de los resaltados especulares, establezca el miembro especular en el color RGBA deseado: los colores más comunes son blanco o gris claro. Los valores establecidos en el miembro Power controlan la niguidad de los efectos especulares.

Los resaltados especulares pueden crear efectos drásticos. Dibujar de nuevo en la analogía azul: un valor de potencia mayor crea resaltados especulares más nítidos, lo que hace que el cristal parezca ser bastante brillante. Los valores más pequeños aumentan el área del efecto, lo que crea una reflexión descarada que hace que el cristal parezca desatezado. Para que un objeto sea realmente una sombra, establezca el miembro Power en cero y el color de Specular en negro. Experimente con diferentes niveles de reflexión para generar una apariencia realista para sus necesidades. En la ilustración siguiente se muestran dos modelos idénticos. El de la izquierda usa una potencia de reflexión especular de 10; El modelo de la derecha no tiene ninguna reflexión especular.

![ilustración de modelos de reflexión especular](images/spechigh.png)

## <a name="setting-material-properties"></a>Establecer propiedades de material

Los dispositivos de representación de Direct3D se pueden representar con un conjunto de propiedades de material a la vez.

En una aplicación de C++, para establecer las propiedades de material que usa el sistema, prepare una estructura [**D3DMATERIAL9**](d3dmaterial9.md) y, a continuación, llame al método [**IDirect3DDevice9::SetMaterial.**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)

Para preparar la [**estructura D3DMATERIAL9**](d3dmaterial9.md) para su uso, establezca la información de propiedad en la estructura para crear el efecto deseado durante la representación. En el ejemplo de código siguiente se configura la **estructura D3DMATERIAL9** para un material púrpura con resaltados especulares blanco nítidos.


```
D3DMATERIAL9 mat;

// Set the RGBA for diffuse reflection.
mat.Diffuse.r = 0.5f;
mat.Diffuse.g = 0.0f;
mat.Diffuse.b = 0.5f;
mat.Diffuse.a = 1.0f;

// Set the RGBA for ambient reflection.
mat.Ambient.r = 0.5f;
mat.Ambient.g = 0.0f;
mat.Ambient.b = 0.5f;
mat.Ambient.a = 1.0f;

// Set the color and sharpness of specular highlights.
mat.Specular.r = 1.0f;
mat.Specular.g = 1.0f;
mat.Specular.b = 1.0f;
mat.Specular.a = 1.0f;
mat.Power = 50.0f;

// Set the RGBA for emissive color.
mat.Emissive.r = 0.0f;
mat.Emissive.g = 0.0f;
mat.Emissive.b = 0.0f;
mat.Emissive.a = 0.0f;
```



Después de preparar [**la estructura D3DMATERIAL9,**](d3dmaterial9.md) aplique las propiedades llamando al método [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) del dispositivo de representación. Este método acepta la dirección de una estructura **D3DMATERIAL9** preparada como su único parámetro. Puede llamar a **IDirect3DDevice9::SetMaterial** con información nueva según sea necesario para actualizar las propiedades de material del dispositivo. En el ejemplo de código siguiente se muestra cómo podría tener este aspecto en el código.


```
// This code example uses the material properties defined for 
// the mat variable earlier in this topic. The pd3dDev is assumed
// to be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
hr = pd3dDev->SetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



Al crear un dispositivo Direct3D, el material actual se establece automáticamente en el valor predeterminado que se muestra en la tabla siguiente.



| Miembro   | Valor                |
|----------|----------------------|
| Difusa  | (R:0, G:0, B:0, A:0) |
| Especular | (R:0, G:0, B:0, A:0) |
| Ambiente  | (R:0, G:0, B:0, A:0) |
| Emisor de luz | (R:0, G:0, B:0, A:0) |
| Potencia    | (0.0)                |



 

## <a name="retrieving-material-properties"></a>Recuperar propiedades de material

Para recuperar las propiedades de material que el dispositivo de representación está usando actualmente, llame al método [**IDirect3DDevice9::GetMaterial**](/windows/desktop/api) para el dispositivo. A diferencia [**del método IDirect3DDevice9::SetMaterial,**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) **IDirect3DDevice9::GetMaterial** no requiere preparación. El **método IDirect3DDevice9::GetMaterial** acepta la dirección de una estructura [**D3DMATERIAL9**](d3dmaterial9.md) y rellena la estructura proporcionada con información que describe las propiedades de material actuales antes de volver.


```
// For this example, the pd3dDev variable is assumed to 
// be a valid pointer to an IDirect3DDevice9 interface.
HRESULT hr;
D3DMATERIAL9 mat;

hr = pd3dDev->GetMaterial(&mat);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



> [!Note]  
> Si la aplicación no especifica propiedades de material para la representación, el sistema usa un material predeterminado. El material predeterminado refleja toda la luz difusa (blanco, por ejemplo) sin reflexión ambiental o especular y sin color emisivo.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Luces y materiales](lights-and-materials.md)
</dt> </dl>

 

 
