---
description: Operadores de asignación de multiplicación.
ms.assetid: 4d25cef1-8b39-42db-80df-c749940feb0b
title: Operator * = operadores
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 486e85ae8f541c802e50c38d29cd16beb746b587
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696704"
---
# <a name="operator--operators"></a>Operator = (operador) \*

Operadores de asignación y multiplicación

### <a name="overload-list"></a>Lista de sobrecarga



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Operator</th>
<th style="text-align: left;">Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ff729806(v=vs.85)"><strong>XMVECTOR:: Operator * = (XMVECTOR&, float)</strong></a></td>
<td style="text-align: left;">Multiplica una <code>XMVECTOR</code> instancia por un valor de punto flotante y devuelve una referencia a la instancia actualizada. <br/> <code>operator *=</code>Multiplica cada componente de la instancia actual del <a href="xmvector-data-type.md"><strong>tipo de datos XMVECTOR</strong></a> por un valor de punto flotante especificado y devuelve una referencia a la instancia actual actualizada. <br/>
<blockquote>
[!Note]<br />
Este operador solo está disponible en C++.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421388(v=vs.85)"><strong>XMVECTOR:: Operator * = (XMVECTOR&, XMVECTOR)</strong></a></td>
<td style="text-align: left;">Multiplica una <code>XMVECTOR</code> instancia por una segunda instancia, devolviendo una referencia a la instancia inicial actualizada. <br/> El <code>operator *=</code> multiplica cada componente de la instancia actual del <a href="xmvector-data-type.md"><strong>tipo de datos XMVECTOR</strong></a> por el componente correspondiente de una segunda instancia especificada de <code>XMVECTOR</code> , y devuelve una referencia a la instancia inicial actualizada. <br/>
<blockquote>
[!Note]<br />
Este operador solo está disponible en C++.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="see-also"></a>Vea también

<dl> <dt>

[Operadores XMVECTOR](ovw-xmvector-operators.md)
</dt> <dt>

**Referencia**
</dt> <dt>

[**XMVECTOR, tipo de datos**](xmvector-data-type.md)
</dt> </dl>

 

 
