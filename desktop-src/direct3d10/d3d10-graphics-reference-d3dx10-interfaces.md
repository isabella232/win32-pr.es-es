---
description: Esta sección contiene información de referencia de las interfaces del modelo de objetos componentes (COM) proporcionadas por la biblioteca de utilidades de D3DX. Las interfaces siguientes se usan con la biblioteca de utilidades de D3DX.
ms.assetid: c57d9c39-3f30-4205-9b0a-665fe53f2b14
title: Interfaces de D3DX (gráficos de Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e4e0fc152468efec4e33fd6a3ab467d211cfbef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652339"
---
# <a name="d3dx-interfaces-direct3d-10-graphics"></a>Interfaces de D3DX (gráficos de Direct3D 10)

Esta sección contiene información de referencia de las interfaces del modelo de objetos componentes (COM) proporcionadas por la biblioteca de utilidades de D3DX. Las interfaces siguientes se usan con la biblioteca de utilidades de D3DX.



| Interfaces                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaz ID3DX10DataLoader**](id3dx10dataloader.md)       | Objeto de carga de datos utilizado por la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para cargar datos de forma asincrónica.<br/>                                                                                                                                                                                                                                                                                                   |
| [**Interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md) | Objeto de procesamiento de datos utilizado por la [**interfaz ID3DX10ThreadPump**](id3dx10threadpump.md) para procesar datos cargados de forma asincrónica.<br/>                                                                                                                                                                                                                                                                                      |
| [**Interfaz ID3DX10Font**](id3dx10font.md)                   | La interfaz ID3DX10Font encapsula las texturas y los recursos necesarios para representar una fuente específica en un dispositivo específico.<br/>                                                                                                                                                                                                                                                                                                |
| [**Interfaz ID3DX10Mesh**](id3dx10mesh.md)                   | Las aplicaciones usan los métodos de la interfaz ID3DX10Mesh para manipular los objetos de malla.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**Interfaz ID3DX10MeshBuffer**](id3dx10meshbuffer.md)       |                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**Interfaz ID3DX10SkinInfo**](id3dx10skininfo.md)           | ID3DX10SkinInfo permite optimizar, procesar y establecer manualmente la relación entre los huesos y los vértices de las mallas (consulte la [animación del esqueleto en Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)). Es más útil para hacer que los archivos. x exportados por las aplicaciones de DCC (por ejemplo, 3DS Max y Maya) sean más fáciles de utilizar para el hardware y para mejorar la velocidad de representación de las mallas estratificadas en el modo de representación de software.<br/> |
| [**Interfaz ID3DX10Sprite**](id3dx10sprite.md)               | La interfaz ID3DX10Sprite proporciona un conjunto de métodos que simplifican el proceso de dibujar sprites mediante Microsoft Direct3D.<br/>                                                                                                                                                                                                                                                                                            |
| [**Interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)       | Se utiliza para ejecutar tareas de forma asincrónica. Este objeto ocupa una cantidad considerable de recursos, por lo que generalmente solo se debe crear uno por aplicación.<br/>                                                                                                                                                                                                                                                                  |
| [**Interfaz ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)   | Las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matriz.<br/>                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de D3DX](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 




