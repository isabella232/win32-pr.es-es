---
title: Barra de título (referencia de elementos de interfaz de usuario de MSAA)
description: En la barra de título de la parte superior de una ventana se muestra un icono y una línea de texto definidos por la aplicación.
ms.assetid: f41ab777-6c94-4d8e-b743-c635e93df396
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1fee3642a67be85b27eac6a73ac7c452f2349d1
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/11/2020
ms.locfileid: "104420181"
---
# <a name="title-bar-msaa-ui-element-reference"></a>Barra de título (referencia de elementos de interfaz de usuario de MSAA)

> [!Note]  
> En este tema se describen los objetos de **barra de título** para la referencia de elementos de interfaz de usuario de MSAA. La forma de crear objetos de **barra de título** en varios marcos de interfaz de usuario no se describe aquí. Consulte la documentación de referencia de la API del marco de interfaz de usuario que está usando.

 

En la barra de título de la parte superior de una ventana se muestra un icono y una línea de texto definidos por la aplicación. El texto especifica el nombre de la aplicación e indica el propósito de la ventana. La barra de título también permite que el usuario mueva la ventana con un mouse u otro dispositivo señalador.

Las barras de título contienen al menos tres botones pequeños que minimizan, maximizan o restauran, y cierran la ventana asociada a la barra de título. Las barras de título también contienen un botón ayuda contextual. Las aplicaciones que se ejecutan en la versión Far-East del sistema operativo Windows también pueden contener botones del editor de métodos de entrada (IME). Microsoft Active Accessibility expone estos botones como elementos secundarios de la barra de título.

## <a name="iaccessible-methods"></a>Métodos IAccessible

Las barras de título admiten los siguientes métodos [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :

-   [**accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest)
-   [**accLocation**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acclocation)
-   [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
-   [**accSelect**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accselect)

## <a name="iaccessible-properties"></a>Propiedades de IAccessible

Las barras de título admiten las siguientes propiedades [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) :



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
<td>La propiedad <strong>ChildCount</strong> es cinco. La propiedad <strong>ChildCount</strong> incluye los botones IME y ayuda contextual incluso cuando no se muestran. Los botones que no se muestran tienen la propiedad <strong>State</strong> <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accDescription</strong></td>
<td>La propiedad <strong>Description</strong> de la propia barra de título es: &quot; muestra el nombre de la ventana y contiene controles para manipularla. &quot; Los botones secundarios de la barra de título tienen las siguientes descripciones:<br/>
<ul>
<li>&quot;Saca la ventana del</li>
<li>&quot;Hace que la ventana esté completa</li>
<li>&quot;Coloca un minimizado o</li>
<li>&quot;Cierra la ventana&quot;</li>
<li>&quot;Entra o sale del contexto-</li>
<li>&quot;Muestra el teclado cuando se presiona&quot;</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>get_accName</strong></td>
<td>La barra de título no admite la propiedad <strong>Name</strong> . Los botones secundarios de la barra de título tienen los nombres siguientes:
<ul>
<li>&quot;Minimizar&quot;</li>
<li>&quot;Maximizar &quot; o &quot; restaurar &quot; ,</li>
<li>&quot;Close&quot;</li>
<li>&quot;Ayuda contextual&quot;</li>
<li>&quot;IME&quot;</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>get_accParent</strong></td>
<td>La propiedad <strong>primaria</strong> de la barra de título es la ventana principal de la aplicación ( <a href="object-roles.md"><strong>ROLE_SYSTEM_WINDOW</strong></a> ) que tiene el mismo nombre de clase de ventana definida por la aplicación que la barra de título.</td>
</tr>
<tr class="odd">
<td><strong>get_accRole</strong></td>
<td>La propiedad de <strong>rol</strong> es <a href="object-roles.md"><strong>ROLE_SYSTEM_TITLEBAR</strong></a>. Los botones secundarios de la barra de título tienen la propiedad de <strong>rol</strong> <a href="object-roles.md"><strong>ROLE_SYSTEM_PUSHBUTTON</strong></a>.</td>
</tr>
<tr class="even">
<td><strong>get_accState</strong></td>
<td>La propiedad <strong>Estado</strong> de la barra de título y los botones secundarios puede ser una combinación de uno o varios de los <a href="object-state-constants.md">valores</a>siguientes: <a href="object-state-constants.md"><strong>STATE_SYSTEM_FOCUSABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_INVISIBLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_OFFSCREEN</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_UNAVAILABLE</strong></a>  |  <a href="object-state-constants.md"><strong>STATE_SYSTEM_PRESSED</strong></a><br/></td>
</tr>
<tr class="odd">
<td><strong>get_accValue</strong></td>
<td>La propiedad <strong>Value</strong> es una cadena que es igual que el texto que se muestra en la barra de título.</td>
</tr>
</tbody>
</table>



 

## <a name="notes"></a>Notas

-   Aunque la barra de título de una aplicación tiene el indicador de estado de la marca de la propiedad **State** , nunca tiene el sistema de estado de marca **de estado** [**\_ \_ centrado**](object-state-constants.md). [**\_ \_**](object-state-constants.md) Establecer el foco en un objeto de barra de título se centra en la ventana de la aplicación.
-   Dado que el objeto de barra de título no admite [**Get \_ accChild**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accchild), los botones de la barra de título son elementos simples. No admiten la propia interfaz [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) . El objeto de barra de título proporciona información sobre estos botones secundarios.
-   Dado que las barras de título no obtienen el foco y no tienen ninguna acción predeterminada, los métodos [**accDoDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accdodefaultaction) y [**Get \_ accDefaultAction**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accdefaultaction) no se admiten para este control.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[IAccessible (interfaz)](/windows/desktop/api/oleacc/nn-oleacc-iaccessible)
</dt> </dl>

 

 





