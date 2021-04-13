---
description: Los materiales describen cómo los polígonos reflejan la luz o parecen emitir luz en una escena 3D.
ms.assetid: vs|directx_sdk|~\materials.htm
title: Materiales (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64e75953fd5839e1b3e7b9cc89b7331147cdb585
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104559924"
---
# <a name="materials-direct3d-9"></a>Materiales (Direct3D 9)

Los materiales describen cómo los polígonos reflejan la luz o parecen emitir luz en una escena 3D. Las propiedades de material detallan las características de reflexión difusa, reflexión ambiente, emisión ligera y resaltado especular de un material. Direct3D usa la estructura [**D3DMATERIAL9**](d3dmaterial9.md) para incluir toda la información de propiedades de materiales. A excepción de la propiedad especular, cada propiedad se describe como un color RGBA que representa la cantidad de las partes rojas, verdes y azules de un determinado tipo de luz reflejada y un factor de mezcla alfa.

## <a name="diffuse-and-ambient-reflection"></a>Reflexión difusa y ambiente

Los miembros difusos y ambiente de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) describen cómo un material refleja el ambiente y la luz difusa en una escena. Dado que la mayoría de las escenas contienen mucha más luz difusa que la luz ambiente, la reflexión difusa reproduce la parte más grande al determinar el color. Además, dado que la luz difusa es direccional, el ángulo de incidencia de la luz difusa afecta a la intensidad global de la reflexión. La reflexión difusa es más grande cuando la luz produce un vértice paralelo a la normal del vértice. A medida que aumenta el ángulo, disminuye el efecto del reflejo difuso. La cantidad de luz reflejada es el coseno del ángulo entre la luz entrante y la normal del vértice, tal como se muestra en la siguiente ilustración.

![Ilustración de la cantidad de luz reflejada](images/incident.png)

La reflexión ambiente, como la luz ambiente, no es direccional. La reflexión ambiente tiene un impacto menor en el color aparente de un objeto representado, pero afecta al color general y es más apreciable cuando la luz difusa o ninguna luz no refleja el material. La reflexión ambiente de un material se ve afectada por el conjunto de luz ambiente de una escena llamando al método [**IDirect3DDevice9:: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) con la \_ marca de ambiente D3DRS.

La reflexión difusa y de ambiente funcionan conjuntamente para determinar el color percibido de un objeto, y suelen ser valores idénticos. Por ejemplo, para representar un objeto cristalino azul, cree un material que refleje solo el componente azul de la luz difusa y ambiente. Cuando se coloca en una habitación con una luz blanca, el cristal parece azul. Sin embargo, en un salón que solo tiene luz roja, el mismo cristal parecería negro, porque su material no refleja la luz roja.

## <a name="emission"></a>Emisión

Los materiales se pueden usar para hacer que un objeto representado parezca autoluminosa. El miembro emisor de la estructura [**D3DMATERIAL9**](d3dmaterial9.md) se usa para describir el color y la transparencia de la luz emitida. La emisión afecta al color de un objeto y puede, por ejemplo, hacer un material oscuro más brillante y tomar parte del color emitido.

Puede usar la propiedad emisor de un material para agregar la ilusión de que un objeto emite luz, sin incurrir en la sobrecarga computacional de agregar una luz a la escena. En el caso del cristal azul, la propiedad emisor es útil si desea que aparezca el cristal para que se ilumine, pero no se convierta luz en otros objetos de la escena. Recuerde que los materiales con propiedades emisor no emiten luz que se puede reflejar en otros objetos de una escena. Para lograr esta luz reflejada, debe colocar una luz adicional dentro de la escena.

## <a name="specular-reflection"></a>Reflexión especular

La reflexión especular crea resaltados en los objetos, por lo que aparecen de forma brillante. La estructura [**D3DMATERIAL9**](d3dmaterial9.md) contiene dos miembros que describen el color de resaltado especular, así como el brillo general del material. Para establecer el color de los reflejos especulares, establezca el miembro especular en el color RGBA deseado: los colores más comunes son blanco o gris claro. Los valores que se establecen en el control miembro de la potencia controlan la nitidez de los efectos especulares.

Los reflejos especulares pueden crear efectos drásticos. Dibujo de nuevo en la analogía azul de cristal: un valor de potencia mayor crea resaltes especulares más nítidos, lo que parece que el cristal es bastante brillante. Los valores más pequeños aumentan el área del efecto, creando una reflexión mate que hace que la apariencia de cristal sea helada. Para que un objeto sea realmente mate, establezca el miembro de potencia en cero y el color en especular en negro. Experimente con diferentes niveles de reflexión para obtener una apariencia realista para sus necesidades. En la ilustración siguiente se muestran dos modelos idénticos. La parte de la izquierda usa una potencia de reflexión especular de 10; el modelo de la derecha no tiene reflexión especular.

![Ilustración de los modelos de reflexión especular](images/spechigh.png)

## <a name="setting-material-properties"></a>Establecer propiedades de materiales

Los dispositivos de representación de Direct3D se pueden representar con un conjunto de propiedades de material a la vez.

En una aplicación de C++, establezca las propiedades de material que el sistema utiliza mediante la preparación de una estructura [**D3DMATERIAL9**](d3dmaterial9.md) y, a continuación, la llamada al método [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) .

Para preparar la estructura [**D3DMATERIAL9**](d3dmaterial9.md) para su uso, establezca la información de la propiedad en la estructura para crear el efecto deseado durante la representación. En el ejemplo de código siguiente se configura la estructura **D3DMATERIAL9** para un material púrpura con resaltes especulares blancos nítidos.


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



Después de preparar la estructura [**D3DMATERIAL9**](d3dmaterial9.md) , aplique las propiedades llamando al método [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) del dispositivo de representación. Este método acepta la dirección de una estructura **D3DMATERIAL9** preparada como su único parámetro. Puede llamar a **IDirect3DDevice9:: SetMaterial** con la nueva información según sea necesario para actualizar las propiedades de material del dispositivo. En el ejemplo de código siguiente se muestra cómo podría ser el código.


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
| Power    | (0,0)                |



 

## <a name="retrieving-material-properties"></a>Recuperación de propiedades de materiales

Recupera las propiedades de material que el dispositivo de representación está usando actualmente llamando al método [**IDirect3DDevice9:: GetMaterial**](/windows/desktop/api) para el dispositivo. A diferencia del método [**IDirect3DDevice9:: SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial) , **IDirect3DDevice9:: GetMaterial** no requiere preparación. El método **IDirect3DDevice9:: GetMaterial** acepta la dirección de una estructura [**D3DMATERIAL9**](d3dmaterial9.md) y rellena la estructura proporcionada con información que describe las propiedades del material actual antes de devolver.


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
> Si la aplicación no especifica propiedades de material para la representación, el sistema utiliza un material predeterminado. El material predeterminado refleja todos los colores difusos luminosos, por ejemplo, sin reflexión de ambiente o especular y sin color de emisor.

 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Luces y materiales](lights-and-materials.md)
</dt> </dl>

 

 
