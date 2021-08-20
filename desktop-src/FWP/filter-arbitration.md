---
title: Filtro de cláusulas de conciliación
description: El arbitraje de filtros es la lógica integrada en la plataforma de filtrado de Windows (WFP) que se usa para determinar cómo interactúan entre sí los filtros al tomar decisiones de filtrado del tráfico de red.
ms.assetid: d097f307-113e-4dc3-ad59-ddfb85061583
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7640e94440cf040d9ca51b6c639dc66e3e8a767024d6dbcd01b9c0cd2b87a24b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151198"
---
# <a name="filter-arbitration"></a>Filtro de cláusulas de conciliación

El arbitraje de filtros es la lógica integrada en la plataforma de filtrado de Windows (WFP) que se usa para determinar cómo interactúan entre sí los filtros al tomar decisiones de filtrado del tráfico de red.

## <a name="filter-arbitration-behaviors"></a>Filtrar comportamientos de arbitraje

Los siguientes comportamientos caracterizan el sistema de arbitraje de filtros:

-   Se puede inspeccionar todo el tráfico. Ningún tráfico puede omitir los filtros en una capa determinada.
-   Un filtro de llamada puede bloquear el tráfico a través de **un veto,** incluso si un filtro de mayor prioridad lo ha permitido.
-   Varios proveedores pueden inspeccionar el tráfico en la misma capa. Por ejemplo, el firewall seguido de filtros de sistema de detección de intrusiones (IDS) o IPsec seguido de filtros de calidad de servicio (QoS) pueden examinar el tráfico en la misma capa.

## <a name="filtering-model"></a>Modelo de filtrado

Cada capa de filtro se divide en subcapas ordenadas por prioridad (también denominada peso). El tráfico de red atraviesa sub capas desde la prioridad más alta a la prioridad más baja. Los desarrolladores crean y administran sub capas mediante la API de WFP.

Dentro de cada subcapa, los filtros se ordenan por peso. El tráfico de red se indica a los filtros correspondientes, desde el peso más alto al más bajo.

El algoritmo de conciliación de filtros se aplica a todas las subcapas dentro de una capa y la decisión final de filtrado se toma una vez que se han evaluado todas las subcapas. Esto proporciona varias funcionalidades de coincidencia.

Dentro de una subcapa, el filtro de la cláusula de conciliación se realiza de la siguiente manera:

-   Calcule la lista de filtros correspondientes ordenados por peso de mayor a menor.
-   Evalúe los filtros correspondientes en orden hasta que se devuelva un "Permiso" o un "Bloque" (los filtros también pueden devolver "Continuar") o hasta que se agote la lista.
-   Omita los filtros restantes y devuelva la acción del último filtro evaluado.

Dentro de una capa, el filtro de cláusulas de conciliación se realiza de la siguiente manera:

-   Realice el procedimiento de conciliación de filtros en cada subcapa en orden de prioridad más alta a prioridad más baja.
-   Evalúe todas las subcapas incluso si una subcapa de mayor prioridad ha decidido bloquear el tráfico.
-   Devuelve la acción resultante en función de las reglas de directiva descritas en la sección siguiente.

En el diagrama siguiente se muestra una configuración de subcapa de ejemplo. Los cuadros externos representan capas. Los cuadros internos representan sub capas que contienen filtros. El carácter comodín ( \* ) de un filtro significa que todo el tráfico coincide con el filtro.

![configuración de subcapa de ejemplo](images/fwp-sub-config2.png)

La única manera de omitir un filtro es si un filtro de mayor peso ha permitido o bloqueado el tráfico dentro de la misma subcapa. Por el contrario, una manera de asegurarse de que un filtro siempre ve todo el tráfico dentro de una capa es agregar una subcapa que contenga un único filtro que coincida con todo el tráfico.

## <a name="configurable-override-policy"></a>Directiva de invalidación configurable

Las reglas descritas a continuación rigen las decisiones de arbitraje dentro de una capa. El motor de filtros usa estas reglas para decidir cuál de las acciones de subcapa se aplica al tráfico de red.

La directiva básica es la siguiente.

-   Las acciones se evalúan en orden de prioridad de las sub capas de prioridad más alta a prioridad más baja.
-   "Block" invalida "Permit".
-   "Block" es final (no se puede invalidar) y detiene la evaluación. El paquete se descarta.

La directiva básica no admite el escenario de una excepción no reemplazada por un firewall. Los ejemplos típicos de este tipo de escenario son:

-   El puerto de administración remota debe abrirse incluso en presencia de un firewall de terceros.
-   Componentes que requieren que los puertos se abran para funcionar (por ejemplo, Universal Plug and Play UPnP). Si el administrador ha habilitado explícitamente el componente, el firewall no debe bloquear el tráfico de forma silenciosa.

Para admitir los escenarios anteriores, una decisión de filtrado debe ser más difícil de invalidar que otra decisión de filtrado mediante la administración del permiso de invalidación de acción. Este permiso se implementa como marca **FWPS \_ RIGHT ACTION \_ \_ WRITE** y se establece por filtro.

El algoritmo de evaluación mantiene la acción actual ("Permitir" o "Bloquear") junto con la marca **FWPS \_ RIGHT ACTION \_ \_ WRITE.** La marca controla si una subcapa de prioridad inferior puede invalidar la acción. Al establecer o restablecer la marca **FWPS \_ RIGHT ACTION \_ \_ WRITE** en la estructura [FWPS CLASSIFY \_ \_ OUT0,](/windows/win32/api/fwpstypes/ns-fwpstypes-fwps_classify_out0) un proveedor rige cómo se pueden o no invalidar las acciones. Si se establece la marca, indica que se puede invalidar la acción. Si la marca no está presente, la acción no se puede invalidar.



| Acción | Permitir invalidación (se establece \_ FWPS RIGHT \_ ACTION \_ WRITE) | Descripción                                                                                                          |
|--------|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Permitir | Sí                                                | El tráfico se puede bloquear en otra capa inferior. Esto se denomina permiso temporal.<br/>                            |
| Permitir | No                                                 | El tráfico solo se puede bloquear en otra capa inferior mediante una llamada **Veto**. Esto se denomina permiso duro.<br/> |
| Bloquear  | Sí                                                | El tráfico se puede permitir en otra capa inferior. Esto se denomina bloque flexible.<br/>                           |
| Bloquear  | No                                                 | No se puede permitir el tráfico en otra capa inferior. Esto se denomina bloque de disco duro.<br/>                        |



 

La acción de filtro se  puede establecer estableciendo el miembro de tipo en la estructura [**FWPM \_ ACTION0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_action0) en **FWP \_ ACTION \_ BLOCK** o **FWP \_ ACTION \_ PERMIT**. Junto con el tipo de acción, un filtro también expone la marca **FWPM \_ FILTER FLAG CLEAR ACTION \_ \_ \_ \_ RIGHT**. Si se borra esta marca, el tipo de acción es duro y no se puede invalidar excepto cuando un **veto** invalida un permiso duro, como se explica más adelante; de lo contrario, es flexible, que se puede invalidar mediante una acción de prioridad alta.

En la tabla siguiente se muestra el comportamiento predeterminado para las acciones de filtro y llamada.

| Acción         | Comportamiento predeterminado |
|----------------|------------------|
| Permiso de filtro  | Permiso temporal      |
| Permiso de llamada | Permiso temporal      |
| Bloque de filtro   | Bloque de disco duro       |
| Bloque de llamada  | Bloque flexible       |



 

Un **veto es** una acción "Bloquear" devuelta por el filtro cuando se restablecieron la marca **\_ FWPS RIGHT ACTION \_ \_ WRITE** antes de llamar al filtro. Un **veto bloqueará** el tráfico permitido con un permiso seguro.

Cuando se **emite un veto,** es una indicación de conflicto en la configuración. Las siguientes acciones se toman para mitigar el conflicto.

-   El tráfico está bloqueado.
-   Se genera un evento de auditoría.
-   Se genera una notificación.
    > [!Note]  
    > Todas las entidades que se han suscrito a ella reciben la notificación. Normalmente, esto incluirá el firewall (para detectar configuraciones erróneas) o las aplicaciones (con el fin de detectar si se invalida su filtro determinado).

     

    > [!Note]  
    > No se crea ninguna instancia obligatoria de la interfaz de usuario (UI) cuando se invalida un filtro "Permiso obligatorio". Las notificaciones de la invalidación se envían a cualquier proveedor que se haya registrado para recibirlas, lo que permite que los firewalls, o las aplicaciones que crearon los filtros "Permitir", muestren la interfaz de usuario que solicita la acción del usuario. No hay ningún valor en tener una notificación de interfaz de usuario de plataforma para estos eventos de invalidación, ya que los ISV de firewall que no desean bloquear de forma silenciosa pueden hacerlo registrándose en un lugar diferente en WFP o (menos preferido) controlar toda su lógica en un controlador de llamada. Los ISV que creen que preguntar a los usuarios es una buena idea querrán poseer la experiencia del usuario y crear su propia interfaz de usuario.

     

El comportamiento de mitigación descrito anteriormente garantiza que un filtro "Permiso duro" no se invalide de forma silenciosa por un filtro "Bloquear" y cubre el escenario en el que el firewall no permite bloquear un puerto de administración remota. Para invalidar de forma silenciosa los filtros "Permiso de seguridad" un firewall tiene que agregar sus filtros dentro de una subcapa de mayor prioridad.

> [!Note]  
> Puesto que no hay ningún arbitraje entre capas, es posible que el tráfico permitido con "Permiso obligatorio" todavía se bloquee en otra capa. Es responsabilidad del autor de la directiva asegurarse de que se permite el tráfico en cada capa si es necesario.

 

Las aplicaciones de usuario que solicitan que se abran los puertos agregan filtros reemplazables a una subcapa de prioridad baja. El firewall puede suscribirse al filtro para agregar eventos de notificación y agregar un filtro de coincidencia después de la validación del usuario (o directiva).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Asignación del peso del filtro](filter-weight-assignment.md)
</dt> </dl>

 

