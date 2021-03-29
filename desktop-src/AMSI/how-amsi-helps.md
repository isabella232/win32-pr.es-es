---
title: Cómo AMSI ayuda a defender contra malware
description: Como desarrollador de aplicaciones, puede participar activamente en la defensa contra malware. En concreto, puede ayudar a proteger a sus clientes de malware basado en scripts dinámicos y de las vías no tradicionales de cyberattack.
ms.topic: article
ms.date: 02/27/2019
ms.openlocfilehash: 0d6aee30034312073123f5ab14b1924fd01e6eac
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103773686"
---
# <a name="how-the-antimalware-scan-interface-amsi-helps-you-defend-against-malware"></a>Cómo la interfaz de detección antimalware (AMSI) le ayuda a defenderse contra malware

Para obtener una introducción a la interfaz de análisis antimalware de Windows (AMSI), consulte la [interfaz de examen antimalware (Amsi)](antimalware-scan-interface-portal.md).

Como desarrollador de aplicaciones, puede participar activamente en la defensa contra malware. En concreto, puede ayudar a proteger a sus clientes de malware basado en scripts dinámicos y de las vías no tradicionales de cyberattack.

A modo de ejemplo, supongamos que la aplicación admite scripts: acepta scripts arbitrarios y los ejecuta a través de un motor de scripting. En el momento en que un script está listo para ser proporcionado al motor de scripting, la aplicación puede llamar a las API de Windows AMSI para solicitar un análisis del contenido. De este modo, puede determinar con seguridad si el script es malintencionado antes de decidir si desea continuar y ejecutarlo.

Esto es así incluso si el script se generó en tiempo de ejecución. El script (malintencionado o de otro tipo) puede pasar por varios pasos de desofuscación. Pero en última instancia, es necesario proporcionar el motor de scripting con código sin sistema de ofuscación. Y ese es el punto en el que se invocan las API de AMSI.

A continuación se muestra una ilustración de la arquitectura de AMSI, donde su propia aplicación se representa mediante uno de los cuadros de "otra aplicación".

![arquitectura de AMSI](images/AMSI7Archi.jpg)

La interfaz AMSI de Windows está abierta. Lo que significa que cualquier aplicación puede llamarlo; y cualquier motor de antimalware registrado puede procesar el contenido que se le envía.

No es posible limitar la explicación a los motores de scripting. Quizás su aplicación es una aplicación de comunicación y examina los mensajes instantáneos en busca de virus antes de mostrarlos a los clientes. O quizás el software es un juego que valida los complementos antes de instalarlos. Hay muchas oportunidades y escenarios de uso de AMSI.

## <a name="amsi-in-action"></a>AMSI en acción

Echemos un vistazo a AMSI en acción. En este ejemplo, Windows Defender es la aplicación que llama a las API de AMSI. Sin embargo, puede llamar a las mismas API desde su propia aplicación.

A continuación se muestra un ejemplo de un script que usa la técnica de codificación XOR para ocultar su intención (ya sea benigna o no). En esta ilustración, podemos imaginar que este script se ha descargado de Internet.

![script de ejemplo codificado en Base64](images/AMSI8.png)

Para hacer cosas más interesantes, podemos escribir este script manualmente en la línea de comandos para que no haya ningún archivo real que supervisar. Esto refleja lo que se conoce como "amenaza de archivos". No es tan sencillo como analizar archivos en disco. La amenaza puede ser una puerta trasera que solo vive en la memoria de una máquina.

A continuación, vemos el resultado de la ejecución del script en Windows PowerShell. Verá que Windows Defender es capaz de detectar el ejemplo de prueba AMSI en este escenario complicado, simplemente mediante el uso de la firma de ejemplo de prueba estándar AMSI.

![Windows Defender que detecta el ejemplo de prueba AMSI](images/AMSI9proper.png)

## <a name="amsi-integration-with-javascriptvba"></a>Integración de AMSI con JavaScript/VBA

En el flujo de trabajo mostrado a continuación se describe el flujo de un extremo a otro de un ejemplo, en el que se muestra la integración de AMSI con la ejecución de macros en Microsoft Office.

![Integración de AMSI con JavaScript/VBA](images/integ-js-vba.png)

- El usuario recibe un documento que contiene una macro (malintencionada), que eludi los análisis de software antivirus estáticos mediante técnicas como ofuscación, archivos protegidos por contraseña u otros.
- Después, el usuario abre el documento que contiene la macro (malintencionada). Si el documento se abre en la vista protegida, el usuario hace clic en **Habilitar edición** para salir de la vista protegida.
- El usuario hace clic en **Habilitar macros** para permitir que se ejecuten macros.
- A medida que se ejecuta la macro, el tiempo de ejecución de VBA usa un búfer circular para registrar \[ 1 \] datos y parámetros relacionados con las llamadas a las API de Win32, com y VBA.
- Cuando se observan API de Win32 o COM específicas que se consideran de alto riesgo (también denominados *desencadenadores*) \[ 2 \] , se detiene la ejecución de la macro y el contenido del búfer circular se pasa a Amsi.
- El proveedor de servicios antimalware de AMSI registrado responde con un veredicto para indicar si el comportamiento de la macro es malintencionado o no.
- Si el comportamiento no es malintencionado, la ejecución de macros continúa.
- De lo contrario, si el comportamiento es malintencionado, Microsoft Office cierra la sesión en respuesta a la alerta \[ 3 \] y el antivirus puede poner en cuarentena el archivo.

## <a name="what-does-this-mean-for-you"></a>¿Qué significa esto para usted?

En el caso de los usuarios de Windows, cualquier software malintencionado que use técnicas de ofuscación y fraude en los hosts de scripting integrados de Windows 10 se inspeccionará automáticamente a un nivel mucho más profundo que nunca, proporcionando niveles adicionales de protección.

Como desarrollador de aplicaciones, considere la posibilidad de hacer que la aplicación llame a la interfaz AMSI de Windows si desea beneficiarse de (y proteger a sus clientes con) análisis y análisis adicionales de contenido potencialmente malintencionado.

Como proveedor de software antivirus, puede considerar la posibilidad de implementar la compatibilidad con la interfaz AMSI. Cuando lo haga, el motor tendrá mucha información más detallada sobre los datos que las aplicaciones (incluidos los hosts de scripting integrados de Windows 10) consideran potencialmente malintencionados.

## <a name="more-background-info-about-fileless-threats"></a>Más información general acerca de las amenazas con archivos

Puede que le resulte más fácil obtener información general sobre los tipos de amenazas de archivos que Windows AMSI está diseñado para ayudarle a defenderse. En esta sección, echaremos un vistazo al juego tradicional de CAT-and-mouse que se reproduce en el ecosistema de malware.

Usaremos PowerShell como ejemplo. Pero puede aprovechar las mismas técnicas y los mismos procesos que mostraremos con cualquier lenguaje dinámico &mdash; VBScript, Perl, Python, Ruby, etc.

A continuación se muestra un ejemplo de un script de PowerShell malintencionado.

![un ejemplo de un script de PowerShell malintencionado](images/AMSI1.png)

Aunque este script simplemente escribe un mensaje en la pantalla, el malware suele ser más fraudulento. Pero podría escribir fácilmente una firma para detectarla. Por ejemplo, la firma podría buscar la cadena "write-host ' PWND! '" en cualquier archivo que el usuario abra. Excelente: hemos detectado nuestro primer malware.

A pesar de que la primera firma lo detecta, los autores de malware responderán. Responden creando scripts dinámicos como este ejemplo.

![ejemplo de un script dinámico](images/AMSI2.png)

En ese escenario, los autores de malware crean una cadena que representa el script de PowerShell que se va a ejecutar. Pero usan una técnica de concatenación de cadenas simple para romper la firma anterior. Si alguna vez Ve el origen de una página web con carga de anuncios, verá que se usan muchas instancias de esta técnica para evitar el software de bloqueo de anuncios.

Por último, el autor del malware pasa esta cadena concatenada `Invoke-Expression` al &mdash; mecanismo del cmdlet de PowerShell para evaluar los scripts que se componen o se crean en tiempo de ejecución.

En respuesta, el software antimalware comienza a realizar la emulación de lenguaje básico. Por ejemplo, si vemos que se concatenan dos cadenas, se emulará la concatenación de esas dos cadenas y, a continuación, se ejecutarán las firmas en el resultado. Desafortunadamente, se trata de un enfoque bastante frágil, ya que los lenguajes suelen tener muchas formas de representar y concatenar cadenas.

Por lo tanto, después de ser detectado por esta firma, los autores de malware se moverán a algo más complicado, &mdash; por ejemplo, la codificación de contenido de script en Base64, como en el ejemplo siguiente.

![ejemplo de contenido de script en Base64](images/AMSI3.png)

En ingenioso, la mayoría de los motores antimalware implementan también la emulación de descodificación Base64. Por lo tanto, puesto que también implementamos la emulación de descodificación de Base64, nos preparamos una vez.

En respuesta, los autores de malware se mueven a ofuscación algorítmica &mdash; , como un sencillo mecanismo de codificación XOR en los scripts que ejecutan.

![ejemplo de un script de ofuscación algorítmica](images/AMSI4.png)

Llegados a este punto, por lo general, los motores antivirus se emularán o detectarán, por lo que no se detectará necesariamente lo que está haciendo este script. Sin embargo, podemos empezar a escribir firmas en las técnicas de ofuscación y codificación. De hecho, eso es lo que tiene en cuenta la inmensa mayoría de las firmas para el malware basado en script.

Pero ¿qué ocurre si el ofuscador es tan trivial que parece un gran número de scripts bien comportados? Una firma para ella generaría un número inaceptable de falsos positivos. Este es un script de *stager* de ejemplo que es demasiado benigno para detectarse por sí solo.

![un script de stager de ejemplo demasiado benigno para detectarlo por sí mismo](images/AMSI5.png)

En ese ejemplo, se está descargando una página web e invocando parte de su contenido. Este es el equivalente en Visual Basic Script.

![equivalente en Visual Basic Script](images/AMSI6.png)

Lo que es peor en estos dos ejemplos es que el motor antivirus Inspeccione los archivos abiertos por el usuario. Si el contenido malintencionado solo vive en la memoria, el ataque podría no ser detectado.

En esta sección se muestran las limitaciones de la detección mediante firmas tradicionales. Sin embargo, mientras que un script malintencionado puede pasar por varios pasos de desofuscación, en última instancia debe proporcionar el motor de scripting con código sin formato y sin ofuscar. Y en ese momento &mdash; , tal y como se describe en la primera sección sobre los &mdash; hosts integrados de scripting de Windows 10, se llama a las API de Amsi para solicitar un análisis de este contenido no protegido. Y la aplicación puede hacer lo mismo.

## <a name="related-resources"></a>Recursos relacionados

* [Amenazas de archivos](/windows/security/threat-protection/intelligence/fileless-threats)
* [Office VBA + AMSI: parte del velo en macros malintencionadas](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/12/office-vba-amsi-parting-the-veil-on-malicious-macros/)
* [Fuera de la vista pero no invisible: derrotar el malware sin archivos con supervisión de comportamiento, AMSI y AV de próxima generación](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/27/out-of-sight-but-not-invisible-defeating-fileless-malware-with-behavior-monitoring-amsi-and-next-gen-av/)
