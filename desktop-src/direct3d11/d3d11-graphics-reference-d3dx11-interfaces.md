---
title: Interfaces D3DX (gráficos de Direct3D 11)
description: Esta sección contiene información de referencia para las interfaces del modelo de objetos componentes (COM) proporcionadas por la biblioteca de utilidades D3DX.
ms.assetid: 0d3be1e6-b558-4586-9440-251a5611d7cd
keywords:
- Interfaces D3DX, Direct3D 11
- interfaces, Direct3D 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd67f82d3198ef25254b3a682c80dc98e0313321
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475749"
---
# <a name="d3dx-interfaces-direct3d-11-graphics"></a>Interfaces D3DX (gráficos de Direct3D 11)

Esta sección contiene información de referencia para las interfaces del modelo de objetos componentes (COM) proporcionadas por la biblioteca de utilidades D3DX.

> [!Note]  
> La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.

 


## <a name="in-this-section"></a>En esta sección




| Tema | Descripción | 
|-------|-------------|
| <a href="id3dx11dataloader.md"><strong>ID3DX11DataLoader</strong></a><br /> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.</blockquote><br /> Objeto de carga de datos utilizado <a href="id3dx11threadpump.md"><strong>por la interfaz ID3DX11ThreadPump</strong></a> para cargar datos de forma asincrónica.<br /> | 
| <a href="id3dx11dataprocessor.md"><strong>ID3DX11DataProcessor</strong></a><br /> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.</blockquote><br /> Objeto de procesamiento de datos utilizado <a href="id3dx11threadpump.md"><strong>por la interfaz ID3DX11ThreadPump</strong></a> para cargar datos de forma asincrónica.<br /> | 
| <a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump</strong></a><br /> | <blockquote>[!Note]<br />La biblioteca de utilidades D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de Windows Store.</blockquote><br /> Un bombeo de subprocesos ejecuta tareas de forma asincrónica. Se crea llamando a <a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump.</strong></a> Hay varias API que toman una bomba de subprocesos opcional como parámetro, como <a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a> y <a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a>; Si pasa una interfaz de bombeo de subprocesos a estas API, las funciones se ejecutarán de forma asincrónica en un subproceso independiente. Especialmente en máquinas con varios procesadores, una bomba de subprocesos puede cargar recursos y procesar datos sin una disminución notable del rendimiento.<br /> | 




 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

 





