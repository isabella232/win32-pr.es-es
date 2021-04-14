---
description: Especificar el protocolo de autenticación
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Especificar el protocolo de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9bb2ec20df1ec398f32f3a1ee17334c10d9735
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496319"
---
# <a name="specifying-the-authentication-protocol"></a>Especificar el protocolo de autenticación

En función de los requisitos de seguridad de su sitio, puede solicitar que el servicio de componentes en cola Compruebe siempre la identidad de un cliente, nunca para comprobar la identidad de un cliente o comprobar la identidad de un cliente solo si el componente está configurado para requerir la autenticación incluso cuando no se tiene acceso a ella a través de una cola.

> [!Note]  
> Para usar un componente en cola en el modo de grupo de trabajo, el nivel de autenticación debe estar establecido en ninguno.

 

## <a name="component-services-administrative-tool"></a>Herramienta administrativa Servicios de componentes

Para especificar el protocolo de autenticación, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en **servicios de componentes**, abra la carpeta **aplicaciones com+** asociada con el equipo que desea administrar.

2.  Haga clic con el botón secundario en la aplicación en cola para la que desea especificar el protocolo de autenticación y, a continuación, haga clic en **propiedades**.

3.  Seleccione la pestaña **puesta en cola** en el cuadro de diálogo Propiedades.

4.  En **autenticación de mensajes de MSMQ**, seleccione el botón de radio asociado al Protocolo de autenticación que desea implementar.

5.  Haga clic en **OK**.

## <a name="visual-basic"></a>Visual Basic

Use el parámetro *AuthLevel* al activar la aplicación en cola como se describe en el [moniker](using-the-queue-moniker.md)de la cola.

## <a name="cc"></a>C/C++

Use el parámetro *AuthLevel* al activar la aplicación en cola como se describe en el [moniker](using-the-queue-moniker.md)de la cola.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad de componentes en cola](queued-components-security.md)
</dt> <dt>

[Limitaciones de seguridad en el modo de grupo de trabajo](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



