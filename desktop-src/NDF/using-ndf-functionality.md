---
title: Uso de la funcionalidad de NDF
description: Microsoft proporciona acceso a la funcionalidad de NDF a través de una API pública. Cuando se produce un problema, la aplicación puede usar esta API para aprovechar esta funcionalidad en el contexto de una aplicación específica.
ms.assetid: db06b9a9-a64a-43ff-9b77-95230208cfd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d85d1386971207330579f5395989e14c4b2315dc578f5bb3509695b99d6e215a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133236"
---
# <a name="using-ndf-functionality"></a>Uso de la funcionalidad de NDF

Microsoft proporciona acceso a la funcionalidad de NDF a través de una API pública. Cuando se produce un problema, la aplicación puede usar esta API para aprovechar esta funcionalidad en el contexto de una aplicación específica.

Hay tres fases para realizar el diagnóstico con NDF: crear un incidente, ejecutar diagnósticos y reparaciones y cerrar el incidente. Esta información general indica qué funciones de NDF pueden ser relevantes para un escenario específico. Puede encontrar información detallada sobre cada función en la sección [Referencia de NDF.](ndf-reference.md)

## <a name="creating-an-incident"></a>Creación de un incidente

Una sesión de diagnóstico de NDF requiere un incidente específico para diagnosticar. Hay varias funciones que se pueden usar para crear un incidente. Elija la función que coincida más estrechamente con lo que la aplicación estaba intentando hacer cuando se produjo el error.

-   [**NdfCreateConnectivityIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident)problemas generales de conectividad a Internet que no necesitan información adicional.
-   [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) / [**NdfCreateWebIncidentEx:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex)conexión a una dirección URL HTTP o HTTPS.
-   [**NdfCreateSharingIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident)acceso a una ruta de acceso UNC o un recurso compartido de archivos.
-   [**NdfCreateDNSIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident)resolución de un nombre de host DNS.
-   [**NdfCreatePnrpIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident)resolución de un nombre pnrp del mismo nivel.
-   [**NdfCreateGroupingIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident)unirse a un grupo punto a punto.
-   [**NdfCreateWinSockIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident)conexión a un destino mediante un socket (cuando ninguna de las otras funciones se aplica específicamente).
-   [**NdfCreateIncident:**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident)se usa cuando ningún otro escenario es adecuado y se conoce la clase auxiliar de NDF específica que se va a invocar (junto con los argumentos que requiere). Se usa principalmente con fines de prueba por parte de los desarrolladores de aplicaciones que han escrito su propia clase auxiliar.

## <a name="running-diagnosis-and-repairs"></a>Ejecutar diagnóstico y reparaciones

Hay dos maneras de iniciar la funcionalidad de diagnóstico y reparación.

-   Uso del Windows Interfaz de usuario (recomendado)

    Cuando se ejecuta en la interfaz de Windows estándar, simplemente puede llamar a la función [**NdfExecuteDiagdiag.**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) El Asistente para NDF iniciará y ayudará al usuario a identificar (y, si es posible, resolver) el problema. La función devolverá una vez finalizado este proceso. La interfaz de usuario es opcionalmente modal para la aplicación.

-   Uso de un Interfaz de usuario personalizado (solo Windows 7 y versiones posteriores)

    Hay diferentes funciones disponibles para su uso en escenarios en los que no se muestra ninguna interfaz de usuario o donde no se usa la experiencia estándar de Windows (como Media Center, aplicaciones insertadas y el símbolo del sistema). Esta opción omite la funcionalidad de experiencia del usuario proporcionada en el Asistente para NDF, que incluye la limitación de los resultados a causas raíz totalmente compatibles, así como la heurística para presentar reparaciones al usuario en el orden recomendado. Al usar estas funciones, debe proporcionar cualquiera de estas funcionalidades usted mismo. También debe asegurarse de liberar la memoria que usan los resultados del diagnóstico.

    Para comenzar el diagnóstico, llame a [**la función NdfDiagnoseIncident.**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) Los problemas encontrados se devolverán a la aplicación como una colección de estructuras [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) que describen las causas principales identificadas y las posibles reparaciones.

    Después de seleccionar una reparación (o pedir al usuario que seleccione una reparación), se debe llamar a [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) para intentar la reparación y determinar si se resolvió el problema.

    En algunos casos, una reparación se puede realizar correctamente, pero no resolverá el problema. En tales casos, se recomienda cerrar el incidente existente y, a continuación, abrir uno nuevo. Esto garantizará que se identifiquen los nuevos problemas sin máscara de la reparación inicial. Por ejemplo, supongamos que no había redes inalámbricas visibles. Después de restablecer el adaptador, las redes inalámbricas son visibles, pero ninguna de ellas está en la lista preferida. Se trata de un nuevo problema que requeriría un nuevo diagnóstico para identificar. Si este segundo intento de diagnóstico no identifica problemas adicionales, se puede intentar una reparación diferente para resolver el problema original o se puede informar al usuario de que el problema no se pudo resolver.

    [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) y [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) son API sincrónicas. Si desea cancelar la actividad iniciada por estas funciones, llame a [**NdfCancelIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident) desde otro subproceso. La función devolverá en el siguiente punto de detención disponible en el proceso de diagnóstico o reparación.

    En cualquier momento, puede llamar opcionalmente a [**NdfGetTraceFile**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile) para recuperar una copia del registro de NDF para la sesión de diagnóstico actual e incluirla con los registros de aplicación. El registro se vacía una vez recuperado y las llamadas posteriores solo recuperarán los eventos que se produjeron después de la última llamada a esta función.

## <a name="closing-an-incident"></a>Cerrar un incidente

Cuando haya terminado de diagnosticar un incidente, llame a [**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident) para liberar los recursos del sistema asociados con la realización de diagnósticos en ese incidente. (Tenga en cuenta que esto no libera los objetos creados por [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident).
