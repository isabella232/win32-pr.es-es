---
description: .
ms.assetid: 11169540-555A-48A9-A4CD-535D5765C005
title: Herramienta de prueba de compatibilidad de Internet Explorer (IECTT)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f25e39263f448c7e11db1be32463b3801e4a8761
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648454"
---
# <a name="internet-explorer-compatibility-test-tool-iectt"></a>Herramienta de prueba de compatibilidad de Internet Explorer (IECTT)

La herramienta de prueba de compatibilidad de Internet Explorer (IECTT) es un componente del [Kit de herramientas de compatibilidad de aplicaciones de Microsoft](/windows-hardware/get-started/adk-install). Esta herramienta puede ayudarle a diagnosticar problemas en las aplicaciones web mostrando problemas en tiempo real y cargando opcionalmente los resultados en una base de datos de ACT. Los resultados incluyen detalles sobre posibles problemas de compatibilidad y vínculos para obtener más información acerca de cada problema de compatibilidad. IECTT también le permite excluir problemas y modificar los atributos disponibles.

## <a name="to-open-iectt"></a>Para abrir IECTT

1.  Instale el [Kit de herramientas de compatibilidad de aplicaciones de Microsoft](/windows-hardware/get-started/adk-install).
2.  Haga clic en **Inicio**, seleccione **programas**, **Microsoft Application Compatibility Toolkit 5,6**, herramientas para **desarrolladores y evaluadores** y, a continuación, haga clic en herramienta de prueba de compatibilidad de **Internet Explorer**.

En las secciones siguientes se describen los escenarios de IECTT comunes.

## <a name="view-issues-in-real-time"></a>Ver problemas en tiempo real

Puede buscar y ver los problemas basados en Web en tiempo real mientras prueba sus sitios web y aplicaciones web en Windows Internet Explorer 7 y Windows Internet Explorer 8. Después de completar las pruebas, puede ver los resultados en la pantalla de **datos dinámicos** de IECTT.

## <a name="upload-issues-to-your-act-database"></a>Cargar problemas en la base de datos de ACT

Puede cargar los problemas basados en Web en la base de datos de ACT, que procesa la información y le permite ver los resultados en la pantalla de **análisis** del administrador de compatibilidad de aplicaciones.

## <a name="collect-your-compatibility-data"></a>Recopilar los datos de compatibilidad

Puede recopilar los datos de compatibilidad relacionados con la aplicación web y el sitio web mediante la herramienta IECTT con Internet Explorer 7 o Internet Explorer 7.

**Para recopilar los datos de compatibilidad**

1.  Cierre todas las ventanas activas de Windows Internet Explorer.
2.  En IECTT, en la barra de herramientas de la **herramienta de prueba de compatibilidad de Internet Explorer** , haga clic en **Habilitar**.
3.  Abra una ventana de Internet Explorer 7 o Internet Explorer 8.

    Aparece un mensaje que indica que el registro de evaluación de compatibilidad está activado.

4.  Visite los sitios web o aplicaciones web que se necesitan para su uso en su organización. Al visitar cada sitio, la herramienta IECTT muestra, en tiempo real, los posibles problemas de compatibilidad.
5.  En la barra de herramientas de la **herramienta de prueba de compatibilidad de Internet Explorer** , haga clic en **deshabilitar** cuando haya terminado.

    El proceso de registro de compatibilidad finaliza y se detiene.

## <a name="filter-your-issue-results"></a>Filtrar los resultados del problema

Puede filtrar los resultados de IECTT por nombre de objeto, por tipo de problema o por ambos.

**Para filtrar los resultados del problema**

1.  En la pantalla **herramienta de prueba de compatibilidad de Internet Explorer** , haga clic en **filtro**.

    Aparecerá el cuadro de diálogo **filtro de problemas** .

2.  Escriba el nombre del objeto que desea ver en el cuadro **Escriba el nombre del objeto para ver los problemas** .

Para obtener más información acerca de esta herramienta y otras herramientas para desarrolladores, vea [¿Qué es la herramienta de prueba de compatibilidad de Internet Explorer?](/previous-versions/windows/it-pro/windows-7/cc721989(v=ws.10)) en MSDN Library y la entrada [de blog registro de compatibilidad de aplicaciones en IE8](/archive/blogs/ie/application-compatibility-logging-in-ie8) .

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Herramientas para depurar aplicaciones web y complementos](tools-for-debugging-web-applications-and-add-ons.md)
</dt> </dl>

 

 
