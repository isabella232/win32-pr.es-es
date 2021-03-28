---
title: Interfaz ID3DX11DataLoader (D3DX11core. h)
description: Tenga en cuenta que la biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no es compatible con las aplicaciones de la tienda Windows. Objeto de carga de datos utilizado por la interfaz ID3DX11ThreadPump para cargar datos de forma asincrónica.
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- Interfaz ID3DX11DataLoader Direct3D 11
- Interfaz ID3DX11DataLoader Direct3D 11, descrita
topic_type:
- apiref
api_name:
- ID3DX11DataLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68236451bf2ba6f491d17541f7d4ca627f5063c5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149989"
---
# <a name="id3dx11dataloader-interface"></a>Interfaz ID3DX11DataLoader

> [!Note]  
> La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.

 

Objeto de carga de datos utilizado por la [**interfaz ID3DX11ThreadPump**](id3dx11threadpump.md) para cargar datos de forma asincrónica.

## <a name="members"></a>Miembros

La interfaz **ID3DX11DataLoader** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11DataLoader** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ID3DX11DataLoader** tiene estos métodos.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Método</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataloader-decompress.md"><strong>Descomprimir</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Descomprime los datos codificados.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11dataloader-destroy.md"><strong>Borrar</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Destruye el cargador una vez finalizado un elemento de trabajo.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataloader-load.md"><strong>Carga</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La biblioteca de utilidades de D3DX (D3DX 9, D3DX 10 y D3DX 11) está en desuso para Windows 8 y no se admite para aplicaciones de la tienda Windows.
</blockquote>
<br/> Carga los datos de un disco.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Observaciones

Este objeto se puede heredar y sus miembros se pueden redefinir. Esto le permitirá personalizar la API para cargar y descomprimir sus propios formatos de archivo personalizados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>D3DX11core. h</dt> </dl> |
| Biblioteca<br/>                  | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Interfaces de D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

