---
description: Una extensión de complemento de datos adjuntos es el componente de los datos adjuntos que muestra la interfaz de usuario específica del servicio.
ms.assetid: 1cafa02f-f240-476c-8ce2-ba088afaf889
title: Extensiones de complemento de datos adjuntos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55267edcd30f32ad371a4aa276587b4eca06c57
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/05/2021
ms.locfileid: "105670103"
---
# <a name="attachment-snap-in-extensions"></a>Extensiones de complemento de datos adjuntos

Una extensión de complemento de datos adjuntos es el componente de los datos adjuntos que muestra la interfaz de usuario específica del servicio. La extensión del complemento se hospeda en los complementos de configuración de seguridad. La comunicación entre la extensión de datos adjuntos y su host de complemento se controla mediante los mecanismos de MMC estándar que se describen en la documentación de [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .

Además de las interfaces que la extensión del complemento debe admitir para ser una extensión de complemento MMC, una extensión de complemento de datos adjuntos también debe ser compatible con la interfaz COM, [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo). Esta interfaz implementa métodos que indican si hay datos específicos del servicio que se deben guardar en la base de datos de seguridad y, en caso afirmativo, recuperar y guardar estos datos nuevos. Los complementos de configuración de seguridad llaman a métodos de esta interfaz con regularidad para actualizar la base de datos de seguridad.

Los complementos de configuración de seguridad implementan una interfaz, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), que proporciona métodos para recuperar datos específicos del servicio de la base de datos de seguridad. Las extensiones del complemento de datos adjuntos pueden llamar a métodos de esta interfaz para recuperar datos de la base de datos de seguridad.

Esta arquitectura se ilustra en el diagrama siguiente.

![extensiones de complemento de datos adjuntos](images/model2.png)

Al crear una extensión de complemento de datos adjuntos, debe instalarla y registrarla con los complementos de configuración de seguridad. Para ello, agregue claves al registro, como se explica en [registrar una extensión de complemento de datos adjuntos](registering-an-attachment-snap-in-extension.md). Cuando se inicia un complemento de configuración de seguridad, comprueba el registro y carga todas las extensiones de complemento registradas. Las extensiones aparecen como nodos en el área de seguridad de cada servicio en el complemento configuración de seguridad.

> [!Note]
> Una extensión de complemento de datos adjuntos solo puede extender los nodos de servicios. El nodo servicios es el complemento MMC que contiene herramientas para administrar servicios instalados en el sistema. La extensión del complemento de datos adjuntos se declara como subordinado a un tipo de nodo de servicios específico y, a continuación, para cada repetición de ese tipo de nodo de servicios, la consola MMC agrega automáticamente las extensiones de complemento relacionadas.
> 
> Cada extensión del complemento de datos adjuntos posee un nodo de panel de ámbito y el panel de resultados relacionado en MMC.

 

 

 
