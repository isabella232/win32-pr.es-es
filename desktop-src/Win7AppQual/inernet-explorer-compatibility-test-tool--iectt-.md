---
description: Herramienta de prueba de compatibilidad de Internet Explorer (IECTT)
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: Herramienta de prueba de compatibilidad de Internet Explorer (IECTT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3a35b3120e95c668f2808c9c525d0c1d4f89f8f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088293"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a>Herramienta de prueba de compatibilidad de Internet Explorer (IECTT)

La Internet Explorer de prueba de compatibilidad de aplicaciones (IECTT) es un componente del kit [de herramientas de compatibilidad de aplicaciones de Microsoft](/windows-hardware/get-started/adk-install). Esta herramienta puede ayudarle a diagnosticar problemas en las aplicaciones web mostrando problemas en tiempo real y, opcionalmente, cargando los resultados en una base de datos act. Los resultados incluyen detalles sobre posibles problemas de compatibilidad y vínculos para obtener más información sobre cada problema de compatibilidad. IECTT también permite excluir problemas y modificar los atributos disponibles.

## <a name="to-open-iectt"></a>Para abrir IECTT

1.  Instale el kit [de herramientas de compatibilidad de aplicaciones de Microsoft](/windows-hardware/get-started/adk-install).
2.  Haga clic **en** Inicio , seleccione **Programas,** Microsoft Application Compatibility **Toolkit 5.6,** Herramientas de desarrollador y evaluador **y,** a continuación, haga clic Internet Explorer Herramienta de prueba **de** compatibilidad .

En las secciones siguientes se describen escenarios comunes de IECTT.

## <a name="view-issues-in-real-time"></a>Ver problemas en tiempo real

Puede buscar y ver los problemas basados en web en tiempo real, mientras prueba sus sitios web y aplicaciones web en Windows Internet Explorer 7 y Windows Internet Explorer 8. Después de completar las pruebas, puede ver los resultados en la pantalla **Datos en directo** de IECTT.

## <a name="upload-issues-to-your-act-database"></a>Carga de problemas en la base de datos de ACT

Puede cargar los problemas basados en web en la base de datos ACT, que procesa la información y le permite ver los resultados en la pantalla Analizar del Administrador de compatibilidad de aplicaciones. 

## <a name="collect-your-compatibility-data"></a>Recopilación de los datos de compatibilidad

Puede recopilar datos de compatibilidad relacionados con el sitio web y la aplicación web mediante la herramienta IECTT con Internet Explorer 7 o Internet Explorer 7.

**Para recopilar los datos de compatibilidad**

1.  Cierre todas las ventanas de Windows Internet Explorer activas.
2.  En IECTT, en la barra de herramientas **de la Internet Explorer de pruebas de compatibilidad,** haga clic en **Habilitar**.
3.  Abra una Internet Explorer 7 o Internet Explorer 8.

    Aparece un mensaje que indica que el registro de evaluación de compatibilidad está activado.

4.  Visite los sitios web o las aplicaciones web que su organización necesita para su uso. A medida que visita cada sitio, la herramienta IECTT muestra, en tiempo real, los posibles problemas de compatibilidad.
5.  En la barra **Internet Explorer herramientas de pruebas de** compatibilidad, haga clic **en** Deshabilitar cuando haya terminado.

    El proceso de registro de compatibilidad finaliza y se detiene.

## <a name="filter-your-issue-results"></a>Filtrar los resultados del problema

Puede filtrar cualquiera de los resultados de IECTT por nombre de objeto, por tipo de problema o por ambos.

**Para filtrar los resultados del problema**

1.  En la pantalla **Internet Explorer de prueba de compatibilidad,** haga clic en **Filtrar.**

    Aparece **el cuadro de diálogo** Filtro de problemas.

2.  Escriba el nombre del objeto que desea ver en el cuadro Escriba el nombre del objeto para **ver los problemas.**

Para obtener más información sobre esta herramienta y otras herramientas de desarrolladores, vea [¿Qué](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) es la herramienta de prueba de compatibilidad de Internet Explorer? en MSDN Library y la entrada de blog Registro de compatibilidad de aplicaciones en [IE8.](/archive/blogs/ie/application-compatibility-logging-in-ie8)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas para depurar aplicaciones web y complementos](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
