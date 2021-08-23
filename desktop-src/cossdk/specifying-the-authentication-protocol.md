---
description: Especificar el protocolo de autenticación
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Especificar el protocolo de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86c4688894543a45f49c4af470658da97e30a159c47025398ac7c7ae5e0620e4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119610515"
---
# <a name="specifying-the-authentication-protocol"></a>Especificar el protocolo de autenticación

En función de los requisitos de seguridad del sitio, puede requerir que el servicio de componentes en cola compruebe siempre la identidad de un cliente, que nunca compruebe la identidad de un cliente o que compruebe la identidad de un cliente solo si el componente está configurado para requerir autenticación incluso cuando no se accede a través de una cola.

> [!Note]  
> Para usar un componente en cola en modo de grupo de trabajo, el nivel de autenticación debe establecerse en ninguno.

 

## <a name="component-services-administrative-tool"></a>Herramienta administrativa de servicios de componentes

Para especificar el protocolo de autenticación, siga estos pasos:

1.  En el árbol de consola de la herramienta administrativa Servicios de componentes, en **Servicios** de componentes , abra la carpeta **Aplicaciones COM+** asociada al equipo que desea administrar.

2.  Haga clic con el botón derecho en la aplicación en cola para la que desea especificar el protocolo de autenticación y, a continuación, haga clic en **Propiedades**.

3.  Seleccione la **pestaña Cola en** el cuadro de diálogo de propiedades.

4.  En MSMQ Message Authentication (Autenticación de mensajes de **MSMQ),** seleccione el botón de radio asociado al protocolo de autenticación que desea implementar.

5.  Haga clic en **Aceptar**.

## <a name="visual-basic"></a>Visual Basic

Use el *parámetro AuthLevel* al activar la aplicación en cola como se describe en [Uso del Moniker de cola](using-the-queue-moniker.md).

## <a name="cc"></a>C/C++

Use el *parámetro AuthLevel* al activar la aplicación en cola como se describe en [Uso del Moniker de cola](using-the-queue-moniker.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Seguridad de componentes en cola](queued-components-security.md)
</dt> <dt>

[Limitaciones de seguridad en el modo de grupo de trabajo](security-limitations-in-workgroup-mode.md)
</dt> </dl>

 

 



