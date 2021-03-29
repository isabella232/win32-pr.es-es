---
title: Arbitraje de filtro
description: El arbitraje de filtros es la lógica integrada en la plataforma de filtrado de Windows (WFP) que se usa para determinar el modo en que los filtros interactúan entre sí al tomar decisiones de filtrado del tráfico de red.
ms.assetid: d097f307-113e-4dc3-ad59-ddfb85061583
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fd7df778d1c24b7480de3321e7a1ec126d8e642
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103791404"
---
# <a name="filter-arbitration"></a>Arbitraje de filtro

El arbitraje de filtros es la lógica integrada en la plataforma de filtrado de Windows (WFP) que se usa para determinar el modo en que los filtros interactúan entre sí al tomar decisiones de filtrado del tráfico de red.

## <a name="filter-arbitration-behaviors"></a>Comportamientos de arbitraje de filtro

Los comportamientos siguientes caracterizan el sistema de arbitraje de filtros:

-   Se puede inspeccionar todo el tráfico. Ningún tráfico puede omitir los filtros en una capa determinada.
-   Un filtro de llamada puede bloquear el tráfico a través de una **veto** , incluso si un filtro de prioridad más alto lo ha permitido.
-   Varios proveedores pueden inspeccionar el tráfico en la misma capa. Por ejemplo, el Firewall seguido de los filtros del sistema de detección de intrusiones (IDS) o IPsec seguido de los filtros de calidad de servicio (QoS) puede examinar el tráfico en la misma capa.

## <a name="filtering-model"></a>Modelo de filtrado

Cada capa de filtro se divide en subcapas ordenadas por prioridad (también denominada peso). El tráfico de red atraviesa subcapas de la prioridad más alta a la prioridad más baja. Los desarrolladores crean y administran subcapas mediante la API de WFP.

Dentro de cada subcapa, los filtros se ordenan por peso. El tráfico de red se indica para los filtros coincidentes de mayor a menor peso.

El algoritmo de arbitraje de filtro se aplica a todas las subcapas dentro de una capa y la decisión de filtrado final se realiza una vez evaluadas todas las subcapas. Esto proporciona varias funcionalidades de coincidencia.

Dentro de una subcapa, el arbitraje de filtro se realiza de la siguiente manera:

-   Calcula la lista de filtros coincidentes ordenados por peso de mayor a menor.
-   Evalúe los filtros coincidentes en orden hasta que se devuelva un "permiso" o un "bloque" (los filtros también pueden devolver "Continue") o hasta que se agote la lista.
-   Omitir los filtros restantes y devolver la acción del último filtro evaluado.

Dentro de una capa, el arbitraje de filtro se realiza de la siguiente manera:

-   Realice el arbitraje de filtros en cada subcapa en orden, desde la prioridad más alta a la más baja.
-   Evalúe todas las subcapas incluso si un subnivel de mayor prioridad ha decidido bloquear el tráfico.
-   Devuelva la acción resultante en función de las reglas de directiva descritas en la sección siguiente.

En el diagrama siguiente se muestra una configuración de subcapa de ejemplo. Las cajas exteriores representan capas. Las casillas internas representan subcapas que contienen filtros. El carácter comodín ( \* ) en un filtro significa que todo el tráfico coincide con el filtro.

![configuración de subcapa de ejemplo](images/fwp-sub-config2.png)

La única forma de omitir un filtro es si un filtro de peso superior ha permitido o bloqueado el tráfico dentro de la misma subcapa. Por el contrario, una manera de asegurarse de que un filtro siempre ve todo el tráfico dentro de una capa es agregar una subcapa que contenga un solo filtro que coincida con todo el tráfico.

## <a name="configurable-override-policy"></a>Directiva de invalidación configurable

Las reglas que se describen a continuación rigen las decisiones de arbitraje dentro de una capa. El motor de filtro utiliza estas reglas para decidir cuál de las acciones de subcapa se aplica al tráfico de red.

La Directiva básica es la siguiente.

-   Las acciones se evalúan en orden de prioridad de las subcapas de prioridad más alta a la prioridad más baja.
-   "Block" invalida "Permit".
-   "Block" es final (no se puede invalidar) y detiene la evaluación. El paquete se descarta.

La Directiva básica no admite el escenario de una excepción no reemplazada por un firewall. Algunos ejemplos típicos de este tipo de escenario son:

-   Puerto de administración remota necesario para abrirse incluso en presencia de un firewall de terceros.
-   Componentes que requieren la apertura de puertos para que funcionen (por ejemplo, Universal Plug and Play UPnP). Si el administrador ha habilitado explícitamente el componente, el Firewall no debe bloquear el tráfico de forma silenciosa.

Con el fin de admitir los escenarios anteriores, una decisión de filtrado debe ser más difícil de reemplazar que otra decisión de filtrado mediante la administración del permiso de invalidación de acción. Este permiso se implementa como el marcador de escritura de la **\_ \_ acción \_ derecha FWPS** y se establece por filtro.

El algoritmo de evaluación mantiene la acción actual ("permitir" o "bloque") junto con la marca de escritura de la **\_ \_ acción \_ derecha FWPS** . La marca controla si se permite que una subcapa de prioridad inferior invalide la acción. Al establecer o restablecer la marca **de \_ \_ \_ escritura de la acción de FWPS derecha** en la estructura [FWPS de \_ clasificación \_ OUT0](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_classify_out0) , un proveedor rige cómo se pueden o no se pueden invalidar las acciones. Si se establece la marca, indica que la acción se puede invalidar. Si la marca está ausente, la acción no se puede invalidar.



| Acción | Permitir invalidación ( \_ se establece la escritura de acción derecha de FWPS \_ \_ ) | Descripción                                                                                                          |
|--------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Permitir | Sí                                                | El tráfico se puede bloquear en otra subcapa. Esto se denomina una concesión de software.<br/>                            |
| Permitir | No                                                 | El tráfico solo se puede bloquear en otra subcapa mediante una **veto** de llamada. Esto se conoce como permiso duro.<br/> |
| Bloquear  | Sí                                                | El tráfico se puede permitir en otra subcapa. Esto se denomina bloque flexible.<br/>                           |
| Bloquear  | No                                                 | No se puede permitir el tráfico en otra subcapa. Esto se denomina bloque duro.<br/>                        |



 

La acción de filtrado se puede establecer estableciendo el miembro de **tipo** en la [**estructura FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0) en el **\_ \_ bloque de acción de FWP** o en el **\_ \_ permiso de acción de FWP**. Junto con el tipo de acción, los filtros también exponen la marca FWPM de la marca de filtrado de marca **\_ \_ \_ \_ \_ derecha**. Si esta marca está desactivada, el tipo de acción es difícil y no se puede invalidar, excepto cuando una **veto** invalida un permiso duro, como se explica más adelante en, de lo contrario, se puede invalidar con una acción de prioridad alta.

En la tabla siguiente se muestra el comportamiento predeterminado de las acciones de filtrado y de llamada.

| Acción         | Comportamiento predeterminado |
|----------------|------------------|
| Permitir filtro  | Concesión de software      |
| Permitir llamada | Concesión de software      |
| Bloque de filtro   | Bloque duro       |
| Bloque de llamada  | Bloque de software       |



 

Una **veto** es una acción de "bloque" devuelta por el filtro cuando la marca de escritura de la **\_ \_ acción \_ de FWPS derecha** se restableció antes de llamar al filtro. Una **veto** bloqueará el tráfico que se permitía con un permiso duro.

Cuando se emite una **veto** , es una indicación de conflicto en la configuración. Las siguientes acciones se llevan a cabo para mitigar el conflicto.

-   El tráfico está bloqueado.
-   Se genera un evento de auditoría.
-   Se genera una notificación.
    > [!Note]  
    > La notificación la reciben todas las entidades que se han suscrito a ella. Normalmente, esto incluirá el firewall (para detectar las configuraciones que no son de) o las aplicaciones (con el fin de detectar si se invalida su filtro concreto).

     

    > [!Note]  
    > No se crea una instancia obligatoria de la interfaz de usuario (UI) cuando se invalida un filtro de "permiso". Las notificaciones de la invalidación se envían a cualquier proveedor que se haya registrado para recibirlos, lo que permite a los firewalls o a las aplicaciones que crearon los filtros "permitir" Mostrar la interfaz de usuario para solicitar la intervención del usuario. No hay ningún valor que tenga una notificación de interfaz de usuario de la plataforma para estos eventos de invalidación, ya que los ISV de firewall que no desean bloquearse de forma silenciosa pueden hacerlo mediante el registro en un lugar diferente en WFP, o (menos preferida) controlan toda la lógica en un controlador de llamada. Los ISV que creen que los usuarios tengan una buena idea querrán poseer la experiencia del usuario y crear su propia interfaz de usuario.

     

El comportamiento de mitigación descrito anteriormente garantiza que un filtro de "permiso" no se invalide de forma silenciosa mediante un filtro de "bloque" y trata el escenario en el que el Firewall no puede bloquear un puerto de administración remoto. Para invalidar de forma silenciosa "permiso", el firewall tiene que agregar sus filtros dentro de una subcapa de prioridad más alta.

> [!Note]  
> Dado que no hay ningún arbitraje entre niveles, el tráfico permitido con "permiso duro" todavía puede estar bloqueado en otra capa. Es responsabilidad del autor de la Directiva asegurarse de que se permite el tráfico en cada capa, si es necesario.

 

Las aplicaciones de usuario que solicitan puertos que se van a abrir agregan filtros reemplazables a una subcapa de prioridad baja. El Firewall puede suscribirse al filtro agregar eventos de notificación y agregar un filtro coincidente después de la validación de usuario (o Directiva).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación del peso del filtro](filter-weight-assignment.md)
</dt> </dl>

 

