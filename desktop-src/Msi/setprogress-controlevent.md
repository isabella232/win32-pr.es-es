---
description: El instalador usa el evento SetProgress para publicar información sobre el progreso de la instalación.
ms.assetid: be597c90-7222-4542-b0f7-e9f4cdfc08b9
title: SetProgress ControlEvent,
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acd7523f03dd8fc8216991ae16b05a731e9f38f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104002366"
---
# <a name="setprogress-controlevent"></a>SetProgress ControlEvent,

El instalador usa el evento SetProgress para publicar información sobre el progreso de la instalación. Un [control ProgressBar](progressbar-control.md) o un control de la [cartelera](billboard-control.md) debe suscribirse al evento a través de la [tabla EventMapping](eventmapping-table.md) mediante el nombre de la acción cuyo progreso se está indicando. Este evento debe crearse en la [tabla EventMapping](eventmapping-table.md).

Este ControlEvent, se puede controlar mediante una interfaz de usuario que se ejecuta en la interfaz de usuario [*básica*](b-gly.md), la interfaz de usuario [*reducida*](r-gly.md)o los niveles de [*IU completos*](f-gly.md) . Para obtener información sobre los niveles de interfaz de usuario, consulte niveles de la [interfaz de usuario](user-interface-levels.md).

## <a name="published-by"></a>Publicado por

Este ControlEvent, lo publica el instalador.

## <a name="argument"></a>Argumento

Ninguno.

## <a name="action-on-subscribers"></a>Acción en los suscriptores

Ninguno.

## <a name="typical-use"></a>Uso típico

Un control [ProgressBar](progressbar-control.md) de un cuadro de diálogo no modal se suscribe a este evento mediante el atributo [Progress](progress-control-attribute.md) para recibir la información de progreso.

 

 



