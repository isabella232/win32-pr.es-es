---
description: En esta sección se describe cómo imprimir desde un programa Windows nativo.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 'Cómo: Imprimir desde un programa de Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2999f112285dfff389583b15f7c7c2913a3e125bc58713e2ba5f18973aa6e1ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971344"
---
# <a name="how-to-print-from-a-windows-program"></a>Cómo: Imprimir desde un programa de Windows

En esta sección se describe cómo imprimir desde un programa Windows nativo.

## <a name="overview"></a>Información general

La impresión suele ser una parte integral de un programa Windows nativo. Por lo tanto, no es una característica que pueda agregar fácilmente después de haber escrito el programa. Dicho esto, si el programa está diseñado para usar documentos XPS, no necesitará mucho código adicional, si existe, para representar el contenido del documento para imprimirlo. Los documentos XPS de la aplicación se pueden enviar directamente a una impresora que tenga un controlador de impresora XPSDrv.

Use [la API de documentos XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) para crear el contenido del documento y [xps Print API](xps-printing.md) para enviar el contenido del documento a la impresora. XpS Print API procesa el contenido del documento para la impresora de destino. Si la impresora seleccionada tiene un controlador de impresora XPSDrv, el documento se enviará a la impresora sin ninguna conversión adicional. Si la impresora seleccionada tiene un controlador de impresora basado en GDI, el programa también puede enviar el contenido a la impresora y XPS Print API convierte el contenido del documento para que sea compatible con el controlador de impresora basado en GDI. En cualquier caso, el procesamiento que realiza la aplicación es el mismo.

## <a name="printing-tasks"></a>Tareas de impresión

En los temas siguientes se describen los pasos básicos para imprimir contenido del programa.

1.  **Recopile información del trabajo de impresión del usuario.**

    Normalmente, un usuario inicia un trabajo de impresión cuando selecciona la opción de impresión de un menú y el programa muestra un cuadro de diálogo de impresión para recopilar los detalles del trabajo de impresión. Normalmente, el usuario selecciona la impresora, el número de copias y los detalles de configuración de la impresora, como la impresión en dos caras y el stapling.

    Para obtener información sobre cómo hacerlo, vea [Cómo:](preparing-to-print.md)Recopilar información del trabajo de impresión del usuario .

2.  **Cree el indicador de progreso.**

    Un indicador de progreso proporciona al usuario comentarios sobre cómo progresa el trabajo de impresión. El indicador de progreso puede ser una barra de  progreso que forma parte de un cuadro de diálogo que incluye el botón Cancelar del trabajo, o puede ser una barra de progreso en la barra de estado de la parte inferior de la ventana principal.

    Para obtener información sobre el funcionamiento del indicador de progreso, [vea Cómo: Mostrar el progreso del trabajo de impresión](cancel-dialog-box.md).

    Para obtener más ideas sobre cómo mostrar el progreso del trabajo de impresión, vea la información de las directrices de desarrollo de Windows de la interfaz de usuario [de](/windows/desktop/windows-application-ui-development) la aplicación.

3.  **Inicie el subproceso de impresión.**

    Una vez que el programa ha recopilado la información del trabajo de impresión del usuario, puede iniciar el subproceso de impresión para realizar el procesamiento real del documento para imprimirlo.

    Para obtener información sobre el subproceso de impresión, [vea Cómo: Iniciar y detener un subproceso de impresión](how-to--start-and-stop-a-printing-thread.md).

4.  **Representar datos del trabajo de impresión.**

    El subproceso de impresión representa los datos del documento para imprimirlos. Debe dividir este procesamiento en pasos de procesamiento discretos para que el usuario pueda interrumpir el procesamiento y cancelar el trabajo, así como para no permitir que el subproceso de procesamiento bloquee otros subprocesos y procesos.

    Para obtener información sobre cómo representa los datos del trabajo de impresión, [vea Cómo:](how-to--render-the-print-job-data.md)Representar datos del trabajo de impresión .

5.  **Supervisar el progreso del trabajo de impresión.**

    A medida que se realiza cada paso de procesamiento, actualice la barra de progreso para informar del uso. Calcule los pasos de procesamiento para completar el trabajo solicitado y, a continuación, actualice la barra de progreso a medida que se realizan esos pasos.

6.  **Cierre el trabajo de impresión y finalice el subproceso de impresión.**

    Después de que el programa haya enviado el trabajo de impresión a la impresora, o si el usuario ha cancelado el trabajo de impresión, debe cerrar el trabajo de impresión y liberar los recursos utilizados por el trabajo de impresión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo: Recopilar información del trabajo de impresión del usuario](preparing-to-print.md)
</dt> </dl>

 

 
