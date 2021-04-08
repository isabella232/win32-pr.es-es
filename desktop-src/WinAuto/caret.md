---
title: Símbolo de intercalación (referencia de elementos de interfaz de usuario de MSAA)
description: El símbolo de intercalación es una línea, un bloque o un mapa de bits intermitentes en el área cliente de una ventana o en un control que acepta la entrada del teclado.
ms.assetid: f2c48c36-1859-4e0a-8833-3ca90b4da323
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da3855e4825c6c8b8498f0b4b278a099452baa9d
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/29/2020
ms.locfileid: "103904373"
---
# <a name="caret-msaa-ui-element-reference"></a>Símbolo de intercalación (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los acentos para la referencia de elementos de la interfaz de usuario de MSAA. El uso de las intercalaciones en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

El símbolo de intercalación es una línea, un bloque o un mapa de bits intermitentes en el área cliente de una ventana o en un control que acepta la entrada del teclado. Indica el lugar en el que se insertan texto o gráficos. Dado que solo una ventana a la vez tiene el foco de teclado, solo hay un símbolo de intercalación en el sistema.

## <a name="iaccessible-methods"></a>Métodos IAccessible

El símbolo de intercalación admite los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

El símbolo de intercalación admite las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propiedad</th>
<th>Comentarios</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchildcount"><strong>get_accChildCount</strong></a></td>
<td>La propiedad <strong>ChildCount</strong> es cero.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname"><strong>get_accName</strong></a></td>
<td>La propiedad <strong>Name</strong> es &quot; Edit &quot; .</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole"><strong>get_accRole</strong></a></td>
<td>La propiedad de <strong>rol</strong> es <strong>[ROLE_SYSTEM_CARET](object-roles.md)</strong>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate"><strong>get_accState</strong></a></td>
<td>Los valores posibles para la propiedad <strong>State</strong> incluyen:
<ul>
<li>Cero, lo que significa que el símbolo de intercalación es visible</li>
<li><strong>[STATE_SYSTEM_INVISIBLE](object-state-constants.md)</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>Notas

-   A diferencia de otros elementos de la interfaz de usuario, el objeto de símbolo de intercalación no tiene un identificador de ventana asociado. Para obtener acceso al objeto de símbolo de intercalación, los clientes deben establecer [*WinEventProc*](/windows/desktop/api/Winuser/nc-winuser-wineventproc) y esperar a que el objeto de símbolo de intercalación genere eventos.
-   El objeto de símbolo de intercalación en el control Rich Edit proporcionado por Riched20.dll (que se usa en los editores de texto como Microsoft WordPad en Windows 98) no envía ningún [WinEvents](winevents-infrastructure.md) cuando se cambia su posición durante la selección de texto. Cuando los usuarios presionan Mayús y las teclas de dirección para seleccionar texto, el objeto de símbolo de intercalación no desencadena el [**objeto de evento \_ \_ LOCATIONCHANGE**](event-constants.md) WinEvent. Del mismo modo, cuando la selección se establece mediante programación a través de mensajes Rich Edit, el objeto de símbolo de intercalación no envía ningún evento para indicar su nueva posición.

    Todas las aplicaciones que usan Riched20.dll muestran este problema. Las aplicaciones que usan versiones anteriores del control Rich Edit envían correctamente los eventos en función de la selección.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 




