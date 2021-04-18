---
description: La interfaz de usuario (UI) de tarjeta inteligente es un cuadro de diálogo común que permite al usuario especificar o buscar una tarjeta inteligente para abrirla (es decir, conectarse a una aplicación y usarla en ella).
ms.assetid: a64a617a-b2ae-471f-a88f-a73f0fc3a791
title: Interfaz de usuario de tarjeta inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc558446516149529e9a98d28aa9fe94f80b2777
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668256"
---
# <a name="smart-card-user-interface"></a>Interfaz de usuario de tarjeta inteligente

La interfaz de [*usuario*](../secgloss/u-gly.md) (UI) de tarjeta inteligente es un [*cuadro de diálogo común*](../secgloss/s-gly.md) que permite al usuario especificar o buscar una tarjeta inteligente para abrirla (es decir, conectarse a una aplicación y usarla en ella).

A continuación se muestran dos maneras de utilizar el cuadro de diálogo común. Ambos suponen que se mostrará la interfaz de usuario del cuadro de diálogo. Para obtener más información, vea [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea).

**Para seleccionar una tarjeta inteligente para abrirla**

1.  Declare una variable de tipo **OPENCARDNAME**.
2.  Proporcione suficiente información en el cuadro de diálogo común para restringir la búsqueda de una tarjeta inteligente que esté buscando la aplicación que realiza la llamada. Esto incluye especificar **lpstrGroupNames**, **lpstrCardNames** y **rgguidInterfaces**. También se incluye la especificación de un modo de uso compartido preferido y el protocolo que se debe usar cuando el cuadro de diálogo común se conecta a la tarjeta mediante los miembros **dwShareMode** y **dwPreferredProtocols** de la estructura [**OPENCARDNAME**](/windows/desktop/api/Winscard/ns-winscard-opencardnamea) .
3.  Llame a la función [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) para mostrar el cuadro de diálogo común al usuario. Se mostrará una línea de información de ayuda simple y, si se encuentra una de las tarjetas que se solicitan, la tarjeta se resaltará en la pantalla. En el caso de las búsquedas de varios nombres de tarjeta, se resaltará el primer lector que contenga una de las tarjetas preferidas.
4.  A continuación, el usuario selecciona una tarjeta, hace clic en **Aceptar** y se conecta a la tarjeta inteligente.

**Para buscar una tarjeta específica**

1.  Declare una variable de tipo **OPENCARDNAME**.
2.  Proporcione suficiente información en el cuadro de diálogo común para restringir la búsqueda de una tarjeta inteligente que esté buscando la aplicación que realiza la llamada. Esto incluye especificar **lpstrGroupNames**, **lpstrCardNames** y **rgguidInterfaces**.
3.  Cree las funciones de devolución de llamada **Connect**, **check** y **Disconnect** y establezca los miembros de datos **lpfnConnect**, **lpfnCheck** y **lpfnDisconnect** de forma adecuada.
    > [!Note]  
    > Las tres funciones y los miembros deben estar disponibles al usar el cuadro de diálogo común de esta manera.

     

4.  Llame a la función de cuadro de diálogo común [**GetOpenCardName**](/windows/desktop/api/Winscard/nf-winscard-getopencardnamea) .
5.  El cuadro de diálogo común buscará las tarjetas solicitadas. Si se encuentra un nombre de tarjeta coincidente o una [*cadena ATR*](../secgloss/a-gly.md) , se llamará a las funciones de devolución de llamada **Connect**, **check** y **Disconnect** en la secuencia. Si una tarjeta pasa la rutina **check** (es decir, la devolución de llamada **check** devuelve **true**), esta tarjeta se resalta en la pantalla al usuario.
    > [!Note]  
    > Si se especifican varios nombres de tarjeta, el primer lector que contiene una de las tarjetas solicitadas y pasa la rutina de **comprobación** será la tarjeta seleccionada.

     

6.  Si no se encuentran coincidencias, aparecerá un cuadro de diálogo común.

 

 
