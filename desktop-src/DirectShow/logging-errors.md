---
description: Errores de registro
ms.assetid: 690ea91b-5bc0-45f0-8354-ec625709f7bd
title: Errores de registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76cded9d4cfaedd93e846fec52b07bf5d4eef9a5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127063192"
---
# <a name="logging-errors"></a>Errores de registro

\[Esta API no se admite y puede modificarse o no estar disponible en el futuro.\]

[DirectShow Editing Services](directshow-editing-services.md) (DES) proporciona un mecanismo integrado para registrar los errores que se producen al cargar, construir o representar un proyecto DES. En este artículo se presenta una aplicación de consola de ejemplo que carga un archivo de proyecto XML e intenta representarlo. Si se produce un error, la aplicación imprime un mensaje de error en la ventana de consola. El código de ejemplo presentado en este artículo se basa en el ejemplo que se proporciona en Carga y vista [previa de un Project](loading-and-previewing-a-project.md).

> [!Note]  
> La aplicación no es necesaria para implementar el registro de errores. DES no registra errores a menos que lo solicite explícitamente.

 

En este artículo se supone que comprende la programación de cliente COM y el modelo de escala de tiempo de DES. Además, debe comprender los conceptos básicos de la programación de objetos COM. Para obtener información sobre las escalas de tiempo en DES, vea [El modelo de escala de tiempo](the-timeline-model.md).

Este artículo contiene las secciones siguientes.

-   [Información general sobre el registro de errores](overview-of-error-logging.md)
-   [Crear una clase de registro de errores](creating-an-error-logging-class.md)
-   [Implementación de IAMErrorLog](implementing-iamerrorlog.md)
-   [Establecer el registro de errores](setting-the-error-log.md)
-   [Registro de errores de DES: código de ejemplo](des-error-logging--example-code.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso de DirectShow Editing Services](using-directshow-editing-services.md)
</dt> </dl>

 

 



