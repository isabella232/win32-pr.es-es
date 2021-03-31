---
description: Operadores de multiplicación.
ms.assetid: f8397999-9956-4d11-8705-c95b788a9f03
title: operadores Operator *
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name: ''
api_type:
- NA
api_location: ''
ms.openlocfilehash: 15cdb9d189d110621461c1623b4fd20eaa9e7f5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155428"
---
# <a name="operator--operators"></a>operadores de operador \*

Operadores de multiplicación

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
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421390(v=vs.85)"><strong>XMVECTOR:: Operator * (float, XMVECTOR)</strong></a></td>
<td style="text-align: left;">Multiplica un valor de punto flotante por una instancia de <code>XMVECTOR</code> , devolviendo el resultado a una nueva instancia de <code>XMVECTOR</code> .<br/> El <code>operator *</code> multiplica un valor de punto flotante en cada componente de una instancia de <a href="xmvector-data-type.md"><strong>tipo de datos XMVECTOR</strong></a>, y devuelve una nueva <code>XMVECTOR</code> instancia cuyos componentes contienen el resultado. <br/>
<blockquote>
[!Note]<br />
Este operador solo está disponible en C++.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421391(v=vs.85)"><strong>XMVECTOR:: Operator * (XMVECTOR, float)</strong></a></td>
<td style="text-align: left;">Multiplica una instancia de <code>XMVECTOR</code> por un valor de punto flotante y devuelve el resultado a una nueva instancia de <code>XMVECTOR</code> .<br/> <code>operator *</code>Multiplica cada componente de una instancia de <a href="xmvector-data-type.md"><strong>tipo de datos XMVECTOR</strong></a> por un valor de punto flotante, y devuelve una nueva <code>XMVECTOR</code> instancia cuyos componentes contienen el resultado. <br/>
<blockquote>
[!Note]<br />
Este operador solo está disponible en C++.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="/previous-versions/windows/desktop/legacy/ee421392(v=vs.85)"><strong>XMVECTOR:: Operator * (XMVECTOR, XMVECTOR)</strong></a></td>
<td style="text-align: left;">Multiplica una instancia de <code>XMVECTOR</code> por una segunda instancia, devolviendo el resultado en una tercera instancia. <br/> El <code>operator *</code> multiplica cada componente de una instancia de <a href="xmvector-data-type.md"><strong>tipo de datos XMVECTOR</strong></a> por el componente correspondiente en una segunda instancia de <code>XMVECTOR</code> , y devuelve una nueva <code>XMVECTOR</code> instancia de que contiene el resultado. <br/>
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

 

 
