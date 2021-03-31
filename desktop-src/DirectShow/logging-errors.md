---
description: Errores de registro
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Errores de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "103805629"
---
# <a name="logging-errors"></a>Errores de registro

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

Los [servicios de edición de DirectShow](directshow-editing-services.md) (des) proporcionan un mecanismo integrado para registrar los errores que se producen al cargar, construir o representar un proyecto des. En este artículo se presenta una aplicación de consola de ejemplo que carga un archivo de proyecto XML e intenta representarlo. Si se produce un error, la aplicación imprime un mensaje de error en la ventana de la consola. El código de ejemplo que se presenta en este artículo se basa en el ejemplo que se proporciona en [cargar y obtener una vista previa de un proyecto](loading-and-previewing-a-project.md).

> [!Note]  
> No es necesario que la aplicación implemente el registro de errores. DES no registra los errores a menos que lo solicite explícitamente.

 

En este artículo se supone que entiende la programación del cliente COM y el modelo de la escala de tiempo DES. Además, debe comprender los aspectos básicos de la programación de objetos COM. Para obtener información acerca de las escalas de tiempo en DES, vea [el modelo Timeline](the-timeline-model.md).

Este artículo contiene las secciones siguientes.

-   [Información general sobre el registro de errores](overview-of-error-logging.md)
-   [Crear una clase de registro de errores](creating-an-error-logging-class.md)
-   [Implementación de IAMErrorLog](implementing-iamerrorlog.md)
-   [Configuración del registro de errores](setting-the-error-log.md)
-   [Registro de errores DES: código de ejemplo](des-error-logging--example-code.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Usar servicios de edición de DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



