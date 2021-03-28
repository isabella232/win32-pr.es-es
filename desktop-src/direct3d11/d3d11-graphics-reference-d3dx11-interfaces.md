---
title: Interfaces de D3DX (gráficos de Direct3D 11)
description: Esta sección contiene información de referencia de las interfaces del modelo de objetos componentes (COM) proporcionadas por la biblioteca de utilidades de D3DX.
ms.assetid: 0d3be1e6-b558-4586-9440-251a5611d7cd
keywords:
- Interfaces de D3DX, Direct3D 11
- interfaces, Direct3D 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da2890c3c55d1bac9eba09c046927e432b1a27f8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078691"
---
# <a name="d3dx-interfaces-direct3d-11-graphics"></a>Interfaces de D3DX (gráficos de Direct3D 11)

Esta sección contiene información de referencia de las interfaces del modelo de objetos componentes (COM) proporcionadas por la biblioteca de utilidades de D3DX.

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 


## <a name="in-this-section"></a>En esta sección



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Tema</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="id3dx11dataloader.md"><strong>ID3DX11DataLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Objeto de carga de datos utilizado por la <a href="id3dx11threadpump.md"><strong>interfaz ID3DX11ThreadPump</strong></a> para cargar datos de forma asincrónica.<br/></td>
</tr>
<tr class="even">
<td><a href="id3dx11dataprocessor.md"><strong>ID3DX11DataProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Objeto de procesamiento de datos utilizado por la <a href="id3dx11threadpump.md"><strong>interfaz ID3DX11ThreadPump</strong></a> para cargar datos de forma asincrónica.<br/></td>
</tr>
<tr class="odd">
<td><a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Un bombeo de subprocesos ejecuta las tareas de forma asincrónica. Se crea llamando a <a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a>. Hay varias API que toman un bombeo de subprocesos opcional como parámetro, como <a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a> y <a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a>. Si pasa una interfaz de bombeo de subprocesos a estas API, las funciones se ejecutarán de forma asincrónica en un subproceso independiente. Especialmente en equipos con varios procesadores, un bombeo de subprocesos puede cargar recursos y procesar datos sin una disminución apreciable en el rendimiento.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

 





