---
title: Uso de la funcionalidad NDF
description: Microsoft proporciona acceso a la funcionalidad NDF a través de una API pública. Cuando se produce un problema, la aplicación puede usar esta API para aprovechar esta funcionalidad en el contexto de una aplicación específica.
ms.assetid: db06b9a9-a64a-43ff-9b77-95230208cfd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ca74a8a80f7babca75182625ec71dc1ec47cbc7
ms.sourcegitcommit: c9c66a09eeb9e46311879a5181342e89964c1dd8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/10/2020
ms.locfileid: "104420517"
---
# <a name="using-ndf-functionality"></a>Uso de la funcionalidad NDF

Microsoft proporciona acceso a la funcionalidad NDF a través de una API pública. Cuando se produce un problema, la aplicación puede usar esta API para aprovechar esta funcionalidad en el contexto de una aplicación específica.

Hay tres fases para realizar el diagnóstico con NDF: creación de un incidente, ejecución de diagnósticos y reparaciones y cierre del incidente. Esta información general indica qué funciones NDF pueden ser relevantes para un escenario específico. Puede encontrar información detallada sobre cada función en la sección de [referencia de NDF](ndf-reference.md) .

## <a name="creating-an-incident"></a>Creación de un incidente

Una sesión de diagnóstico NDF requiere un incidente específico para diagnosticar. Hay varias funciones que se pueden usar para crear un incidente. Elija la función que mejor coincida con lo que estaba intentando realizar la aplicación cuando se produjo el error.

-   [**NdfCreateConnectivityIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateconnectivityincident): problemas generales de conectividad a Internet que no necesitan información adicional.
-   [**NdfCreateWebIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincident) / [**NdfCreateWebIncidentEx**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewebincidentex): conectarse a una dirección URL http o https.
-   [**NdfCreateSharingIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatesharingincident): acceso a una ruta UNC o un recurso compartido de archivos.
-   [**NdfCreateDNSIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatednsincident): resolución de un nombre de host DNS.
-   [**NdfCreatePnrpIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatepnrpincident): resolución de un nombre de mismo nivel PNRP.
-   [**NdfCreateGroupingIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreategroupingincident): unirse a un grupo de punto a punto.
-   [**NdfCreateWinSockIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreatewinsockincident): conectarse a un destino mediante un socket (cuando no se aplica específicamente ninguna de las otras funciones).
-   [**NdfCreateIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcreateincident): se usa cuando no es apropiado ningún otro escenario y se conoce la clase auxiliar de NDF específica que se va a invocar (junto con los argumentos que requiere). Se utiliza principalmente con fines de prueba por los desarrolladores de aplicaciones que han escrito su propia clase auxiliar.

## <a name="running-diagnosis-and-repairs"></a>Ejecutar diagnósticos y reparaciones

Hay dos maneras de iniciar la funcionalidad de diagnóstico y reparación.

-   Usar la interfaz de usuario de Windows (recomendado)

    Cuando se ejecuta en la interfaz de usuario estándar de Windows, simplemente puede llamar a la función [**NdfExecuteDiagnosis**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfexecutediagnosis) . El asistente NDF iniciará y ayudará al usuario a identificar (y, si es posible, resolver) el problema. La función devolverá después de que finalice este proceso. Opcionalmente, la interfaz de usuario es modal para la aplicación.

-   Usar una interfaz de usuario personalizada (solo Windows 7 y versiones posteriores)

    Hay diferentes funciones disponibles para su uso en escenarios en los que no se muestra ninguna interfaz de usuario o en los que no se usa la experiencia estándar de Windows (como Media Center, aplicaciones incrustadas y el símbolo del sistema). Esta opción omite la funcionalidad de la experiencia del usuario que se proporciona en el asistente NDF, que incluye la limitación de los resultados a causas raíz totalmente compatibles, así como la heurística para presentar a los usuarios reparaciones en el orden recomendado. Al usar estas funciones, debe proporcionar esta funcionalidad usted mismo. También debe asegurarse de liberar la memoria que usan los resultados del diagnóstico.

    Para iniciar el diagnóstico, llame a la función [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) . Cualquier problema encontrado se devolverá a la aplicación como una colección de estructuras [**RootCauseInfo**](/windows/win32/api/ndattrib/ns-ndattrib-rootcauseinfo) que describen las causas raíz y las posibles reparaciones identificadas.

    Después de seleccionar una reparación (o solicitar al usuario que seleccione una reparación), se debe llamar a [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) para intentar la reparación y determinar si el problema se ha resuelto.

    En algunos casos, una reparación puede realizarse correctamente, pero no resolverá el problema. En tales casos, se recomienda cerrar el incidente existente y, a continuación, abrir uno nuevo. Así se asegurará de que se identifican los nuevos problemas sin máscara de la reparación inicial. Por ejemplo, supongamos que no había ninguna red inalámbrica visible. Después de restablecer el adaptador, las redes inalámbricas están visibles, pero ninguna de ellas se muestra en la lista preferida. Se trata de un problema nuevo que requeriría un nuevo diagnóstico para identificar. Si un segundo intento de diagnóstico no identifica otros problemas, se puede intentar una reparación diferente para resolver el problema original, o bien se puede informar al usuario de que no se pudo resolver el problema.

    [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident) y [**NdfRepairIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfrepairincident) son API sincrónicas. Si desea cancelar la actividad iniciada por estas funciones, llame a [**NdfCancelIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcancelincident) desde otro subproceso. La función devolverá el siguiente punto de detención disponible en el proceso de diagnóstico o reparación.

    En cualquier momento, puede llamar a [**NdfGetTraceFile**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfgettracefile) para recuperar una copia del registro NDF de la sesión de diagnóstico actual e incluirla en los registros de la aplicación. El registro se vacía una vez que se ha recuperado y las llamadas subsiguientes solo recuperarán los eventos que se produjeron después de la última llamada a esta función.

## <a name="closing-an-incident"></a>Cerrar un incidente

Cuando haya terminado de diagnosticar un incidente, llame a [**NdfCloseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfcloseincident) para liberar los recursos del sistema asociados a la realización de diagnósticos en ese incidente. (Tenga en cuenta que esto no libera los objetos creados por [**NdfDiagnoseIncident**](/windows/desktop/api/Ndfapi/nf-ndfapi-ndfdiagnoseincident).
