---
description: Esta sección contiene información de referencia para las interfaces del modelo de objetos componentes (COM) proporcionadas por la biblioteca de utilidades D3DX en Gráficos de Direct3D 10.
ms.assetid: c57d9c39-3f30-4205-9b0a-665fe53f2b14
title: Interfaces D3DX (gráficos de Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c064edce5d5841875eb3148bf74b18f50f93081
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408018"
---
# <a name="d3dx-interfaces-direct3d-10-graphics"></a>Interfaces D3DX (gráficos de Direct3D 10)

Esta sección contiene información de referencia para las interfaces del modelo de objetos componentes (COM) proporcionadas por la biblioteca de utilidades D3DX. Las interfaces siguientes se usan con la biblioteca de utilidades D3DX.



| Interfaces                                                     | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interfaz ID3DX10DataLoader**](id3dx10dataloader.md)       | Objeto de carga de datos usado [**por la interfaz ID3DX10ThreadPump para**](id3dx10threadpump.md) cargar datos de forma asincrónica.<br/>                                                                                                                                                                                                                                                                                                   |
| [**Interfaz ID3DX10DataProcessor**](id3dx10dataprocessor.md) | Objeto de procesamiento de datos utilizado [**por la interfaz ID3DX10ThreadPump para**](id3dx10threadpump.md) procesar los datos cargados de forma asincrónica.<br/>                                                                                                                                                                                                                                                                                      |
| [**Interfaz ID3DX10Font**](id3dx10font.md)                   | La interfaz ID3DX10Font encapsula las texturas y los recursos necesarios para representar una fuente específica en un dispositivo específico.<br/>                                                                                                                                                                                                                                                                                                |
| [**Interfaz ID3DX10Mesh**](id3dx10mesh.md)                   | Las aplicaciones usan los métodos de la interfaz ID3DX10Mesh para manipular objetos de malla.<br/>                                                                                                                                                                                                                                                                                                                                   |
| [**Interfaz ID3DX10MeshBuffer**](id3dx10meshbuffer.md)       |                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [**Interfaz ID3DX10SkinInfo**](id3dx10skininfo.md)           | ID3DX10SkinInfo permite optimizar, procesar y establecer manualmente la relación entre los animales y los vértices de las mallas (consulte Animación de esqueletos en [Wikipedia).](https://en.wikipedia.org/wiki/Skeletal_animation) Resulta muy útil para hacer que los archivos .x exportados por las aplicaciones DCC (como 3DS Max y Maya) sea más fácil de usar en el hardware y para mejorar la velocidad de representación de las mallas con máscara en el modo de representación de software.<br/> |
| [**Interfaz ID3DX10Sprite**](id3dx10sprite.md)               | La interfaz ID3DX10Sprite proporciona un conjunto de métodos que simplifican el proceso de dibujo de sprites mediante Microsoft Direct3D.<br/>                                                                                                                                                                                                                                                                                            |
| [**Interfaz ID3DX10ThreadPump**](id3dx10threadpump.md)       | Se usa para ejecutar tareas de forma asincrónica. Este objeto ocupa una cantidad considerable de recursos, por lo que generalmente solo se debe crear uno por aplicación.<br/>                                                                                                                                                                                                                                                                  |
| [**Interfaz ID3DXMatrixStack**](d3d10-id3dxmatrixstack.md)   | Las aplicaciones usan los métodos de la interfaz ID3DXMATRIXStack para manipular una pila de matrices.<br/>                                                                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de D3DX](d3d10-graphics-reference-d3dx10.md)
</dt> </dl>

 

 




