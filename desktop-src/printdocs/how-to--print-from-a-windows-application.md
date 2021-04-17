---
description: En esta sección se describe cómo imprimir desde un programa de Windows nativo.
ms.assetid: D0AE8FF8-D02D-43D3-80CA-E13EAA894F87
title: 'Cómo: imprimir desde un programa de Windows'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84229823944d7f7104da359b953e579f1b21cdca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105697694"
---
# <a name="how-to-print-from-a-windows-program"></a>Cómo: imprimir desde un programa de Windows

En esta sección se describe cómo imprimir desde un programa de Windows nativo.

## <a name="overview"></a>Información general

La impresión suele ser una parte integral de un programa de Windows nativo. Por lo tanto, no es una característica que se puede agregar fácilmente después de haber escrito el programa. Dicho esto, si el programa está diseñado para usar documentos XPS, no necesitará mucho, si lo hay, código adicional para representar el contenido del documento para imprimirlo. Los documentos XPS de la aplicación se pueden enviar directamente a una impresora que tenga un controlador de impresora XPSDrv.

Use la [API de documento XPS](/previous-versions/windows/desktop/dd316976(v=vs.85)) para crear el contenido del documento y la [API de impresión XPS](xps-printing.md) para enviar el contenido del documento a la impresora. La API de impresión XPS procesa el contenido del documento para la impresora de destino. Si la impresora seleccionada tiene un controlador de impresora XPSDrv, el documento se enviará a la impresora sin ninguna conversión adicional. Si la impresora seleccionada tiene un controlador de impresora basado en GDI, el programa también puede enviar el contenido a la impresora y la API de impresión XPS convierte el contenido del documento para que sea compatible con el controlador de impresora basado en GDI. En cualquier caso, el procesamiento que realiza la aplicación es el mismo.

## <a name="printing-tasks"></a>Tareas de impresión

En los temas siguientes se describen los pasos básicos para imprimir el contenido del programa.

1.  **Recopilar información del trabajo de impresión del usuario.**

    Normalmente, un usuario inicia un trabajo de impresión cuando selecciona la opción Imprimir en un menú y el programa muestra un cuadro de diálogo Imprimir para recopilar los detalles del trabajo de impresión. Normalmente, el usuario selecciona la impresora, el número de copias y los detalles de configuración de la impresora, como la impresión a dos caras y el grapado.

    Para obtener información sobre cómo hacerlo, consulte [Cómo: recopilar información del trabajo de impresión del usuario](preparing-to-print.md).

2.  **Cree el indicador de progreso.**

    Un indicador de progreso proporciona al usuario comentarios sobre cómo progresa el trabajo de impresión. El indicador de progreso puede ser una barra de progreso que forma parte de un cuadro de diálogo que incluye el botón **Cancelar** del trabajo, o bien una barra de progreso en la barra de estado en la parte inferior de la ventana principal.

    Para obtener información acerca del funcionamiento del indicador de progreso, vea [Cómo: mostrar el progreso del trabajo de impresión](cancel-dialog-box.md).

    Para obtener más ideas sobre cómo mostrar el progreso del trabajo de impresión, consulte la información de las instrucciones de desarrollo de la interfaz de usuario de la [aplicación Windows](/windows/desktop/windows-application-ui-development) .

3.  **Inicie el subproceso de impresión.**

    Una vez que el programa ha recopilado la información del trabajo de impresión del usuario, puede iniciar el subproceso de impresión para realizar el procesamiento real del documento para imprimirlo.

    Para obtener información sobre el subproceso de impresión, consulte [Cómo: iniciar y detener un subproceso de impresión](how-to--start-and-stop-a-printing-thread.md).

4.  **Representan los datos del trabajo de impresión.**

    El subproceso de impresión representa los datos del documento para imprimirlos. Debe dividir este procesamiento en pasos de procesamiento discretos para que el usuario pueda interrumpir el procesamiento y cancelar el trabajo, así como no permitir que el subproceso de procesamiento bloquee otros subprocesos y procesos.

    Para obtener información sobre cómo representa los datos del trabajo de impresión, vea [Cómo: representar datos de trabajos de impresión](how-to--render-the-print-job-data.md).

5.  **Supervise el progreso del trabajo de impresión.**

    Cuando se realice cada paso de procesamiento, actualice la barra de progreso para informar del uso. Calcule los pasos de procesamiento para completar el trabajo solicitado y, a continuación, actualice la barra de progreso a medida que se realicen los pasos.

6.  **Cierre el trabajo de impresión y termine el subproceso de impresión.**

    Una vez que el programa ha enviado el trabajo de impresión a la impresora, o si el usuario ha cancelado el trabajo de impresión, debe cerrar el trabajo de impresión y liberar los recursos utilizados por el trabajo de impresión.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Cómo: recopilar información del trabajo de impresión del usuario](preparing-to-print.md)
</dt> </dl>

 

 
