---
description: Especificar el protocolo de autenticación
ms.assetid: 2f469332-6b3e-475a-9ec6-782e1e445672
title: Especificar el protocolo de autenticación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9bb2ec20df1ec398f32f3a1ee17334c10d9735
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361648"
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

5.  Haga clic en **OK**.

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

 

 



