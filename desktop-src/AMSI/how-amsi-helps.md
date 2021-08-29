---
title: Cómo ayuda AMSI a defenderse contra malware
description: Como desarrollador de aplicaciones, puede participar activamente en la defensa contra malware. En concreto, puede ayudar a proteger a los clientes frente a malware dinámico basado en scripts y frente a vías no tradicionales de ciberataque.
ms.topic: article
ms.date: 02/27/2019
ms.openlocfilehash: 6c9ce09fdbf928395e2ca538add5fe7121c5ee49867c29205a9a39bce746a382
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440495"
---
# <a name="how-the-antimalware-scan-interface-amsi-helps-you-defend-against-malware"></a>Cómo la interfaz de examen antimalware (AMSI) le ayuda a defenderse contra malware

Para obtener una introducción a Windows interfaz de examen antimalware (AMSI), vea [Antimalware Scan Interface (AMSI)](antimalware-scan-interface-portal.md).

Como desarrollador de aplicaciones, puede participar activamente en la defensa contra malware. En concreto, puede ayudar a proteger a los clientes frente a malware dinámico basado en scripts y frente a vías no tradicionales de ciberataque.

A modo de ejemplo, supongamos que la aplicación admite scripts: acepta scripts arbitrarios y lo ejecuta a través de un motor de scripting. En el momento en que un script está listo para proporcionarse al motor de scripting, la aplicación puede llamar a las API de AMSI de Windows para solicitar un examen del contenido. De este modo, puede determinar de forma segura si el script es malintencionado o no antes de decidir continuar y ejecutarlo.

Esto es así incluso si el script se generó en tiempo de ejecución. El script (malintencionado o de otro tipo) puede pasar por varios pases de desuso. Pero, en última instancia, debe proporcionar al motor de scripting código sin formato y sin ofuscar. Y ese es el punto en el que se invocan las API de AMSI.

Esta es una ilustración de la arquitectura amsi, donde su propia aplicación se representa mediante uno de los cuadros "Otra aplicación".

![la arquitectura amsi](images/AMSI7Archi.jpg)

La Windows de AMSI está abierta. Lo que significa que cualquier aplicación puede llamarla; y cualquier motor antimalware registrado puede procesar el contenido que se le envía.

Tampoco es necesario limitar la discusión a los motores de scripting. Quizás la aplicación es una aplicación de comunicación y examina los mensajes instantáneos en busca de virus antes de que se muestre a los clientes. O quizás el software sea un juego que valide los complementos antes de instalarlos. Hay muchas oportunidades y escenarios para usar AMSI.

## <a name="amsi-in-action"></a>AMSI en acción

Echemos un vistazo a AMSI en acción. En este ejemplo, Windows Defender es la aplicación que llama a las API de AMSI. Pero puede llamar a las mismas API desde dentro de su propia aplicación.

Este es un ejemplo de un script que usa la técnica de codificación XOR para ocultar su intención (independientemente de si esa intención es benigna o no). En esta ilustración, podemos imaginar que este script se descargó de Internet.

![script de ejemplo codificado en Base64](images/AMSI8.png)

Para que las cosas más interesantes, podemos escribir este script manualmente en la línea de comandos para que no haya ningún archivo real para supervisar. Esto refleja lo que se conoce como una "amenaza sin archivos". No es tan sencillo como examinar archivos en disco. La amenaza podría ser una puerta trasera que solo se encuentra en la memoria de una máquina.

A continuación, vemos el resultado de ejecutar el script en Windows PowerShell. Verá que Windows Defender el ejemplo de prueba de AMSI en este escenario complicado, simplemente mediante la firma de ejemplo de prueba de AMSI estándar.

![Windows Defender el ejemplo de prueba de AMSI](images/AMSI9proper.png)

## <a name="amsi-integration-with-javascriptvba"></a>Integración de AMSI con JavaScript/VBA

En el flujo de trabajo que se muestra a continuación se describe el flujo de un extremo a otro ejemplo, en el que se muestra la integración de AMSI con la ejecución de macros Microsoft Office.

![Integración de AMSI con JavaScript/VBA](images/integ-js-vba.png)

- El usuario recibe un documento que contiene una macro (malintencionada) que evita los exámenes de software antivirus estáticos mediante técnicas como ofuscación, archivos protegidos con contraseña u otros.
- A continuación, el usuario abre el documento que contiene la macro (malintencionada). Si el documento se abre en vista protegida, el usuario hace clic en **Habilitar** edición para salir de la vista protegida.
- El usuario hace clic en **Habilitar macros** para permitir la ejecución de macros.
- A medida que se ejecuta la macro, el tiempo de ejecución de VBA usa un búfer circular para registrar 1 datos y parámetros relacionados con las llamadas a las API \[ \] de Win32, COM y VBA.
- Cuando se observan api de Win32 o COM específicas que se consideran de alto riesgo (también conocidas como desencadenadores *)* 2, la ejecución de macros se detiene y el contenido del búfer circular se pasa a \[ \] AMSI.
- El proveedor de servicios antimalware de AMSI registrado responde con un veredicto para indicar si el comportamiento de la macro es malintencionado o no.
- Si el comportamiento no es malintencionado, la ejecución de macros continúa.
- De lo contrario, si el comportamiento es malintencionado, Microsoft Office cerrará la sesión en respuesta a la alerta 3 y el av puede poner en cuarentena \[ \] el archivo.

## <a name="what-does-this-mean-for-you"></a>¿Qué significa esto para usted?

Para los usuarios de Windows, cualquier software malintencionado que use técnicas de ofuscación y fraude en los hosts de scripting integrados de Windows 10 se inspecciona automáticamente en un nivel mucho más profundo que nunca, lo que proporciona niveles adicionales de protección.

Para usted como desarrollador de aplicaciones, considere la posibilidad de que la aplicación llame a la interfaz amsi de Windows si desea beneficiarse de (y proteger a sus clientes con) análisis y análisis adicionales de contenido potencialmente malintencionado.

Como proveedor de software antivirus, puede considerar la posibilidad de implementar la compatibilidad con la interfaz AMSI. Cuando lo haga, el motor tendrá información mucho más detallada sobre los datos que las aplicaciones (incluidos los hosts de scripting integrados de Windows 10) consideran potencialmente malintencionados.

## <a name="more-background-info-about-fileless-threats"></a>Más información general sobre las amenazas sin archivos

Es posible que tenga curiosidad por obtener más información sobre los tipos de amenazas sin archivos que Windows AMSI está diseñado para ayudarle a defenderse. En esta sección, echaremos un vistazo al juego tradicional de gatos y mouse que se reproduce en el ecosistema de malware.

Usaremos PowerShell como ejemplo. Pero puede aprovechar las mismas técnicas y procesos que mostraremos con cualquier &mdash; lenguaje dinámico VBScript, Perl, Python, Ruby, etc.

Este es un ejemplo de un script de PowerShell malintencionado.

![un ejemplo de un script de PowerShell malintencionado](images/AMSI1.png)

Aunque este script simplemente escribe un mensaje en la pantalla, el malware suele ser más malintencionado. Pero podría escribir fácilmente una firma para detectar esta. Por ejemplo, la firma podría buscar la cadena "Write-Host 'pwnd!'". en cualquier archivo que abra el usuario. Excelente: hemos detectado nuestro primer malware.

Sin embargo, después de que la primera firma lo detecte, los autores de malware responderán. Responden mediante la creación de scripts dinámicos como este ejemplo.

![un ejemplo de un script dinámico](images/AMSI2.png)

En ese escenario, los autores de malware crean una cadena que representa el script de PowerShell que se ejecutará. Pero usan una técnica simple de concatenación de cadenas para interrumpir la firma anterior. Si alguna vez ve el origen de una página web cargada de anuncios, verá que se usan muchas instancias de esta técnica para evitar el bloqueo de software.

Por último, el autor de malware pasa esta cadena concatenada al mecanismo de PowerShell del cmdlet para evaluar los scripts que se componen o `Invoke-Expression` crean en tiempo de &mdash; ejecución.

En respuesta, el software antimalware empieza a realizar la emulación básica del lenguaje. Por ejemplo, si vemos dos cadenas concatenadas, emulamos la concatenación de esas dos cadenas y, a continuación, ejecutamos nuestras firmas en el resultado. Desafortunadamente, se trata de un enfoque bastante frágil, ya que los lenguajes tienden a tener muchas maneras de representar y concatenar cadenas.

Por lo tanto, después de ser capturados por esta firma, los autores de malware pasarán a algo más complicado, por ejemplo, codificar el contenido del script en Base64, como en &mdash; este ejemplo siguiente.

![un ejemplo de contenido de script en Base64](images/AMSI3.png)

Al tener recursos, la mayoría de los motores antimalware también implementan la emulación de la decodificación de Base64. Por lo tanto, puesto que también implementamos la emulación de la decodificación de Base64, vamos por delante durante un tiempo.

En respuesta, los autores de malware se mueven a ofuscación algorítmica, como un mecanismo simple de codificación &mdash; XOR en los scripts que ejecutan.

![un ejemplo de script de ofuscación algorítmica](images/AMSI4.png)

En este punto, generalmente hemos pasado lo que los motores antivirus emularán o detectarán, por lo que no detectaremos necesariamente lo que está haciendo este script. Sin embargo, podemos empezar a escribir firmas contra las técnicas de ofuscación y codificación. De hecho, eso es lo que representa la gran mayoría de las firmas de malware basado en scripts.

Pero,¿qué ocurre si el ofuscador es tan trivial que se parece a muchos scripts bien comportados? Una firma para ella generaría un número inaceptable de falsos positivos. Este es un script *de stager* de ejemplo que es demasiado benigno para detectar por sí mismo.

![un script de stager de ejemplo que es demasiado benigno para detectar por sí mismo](images/AMSI5.png)

En ese ejemplo, vamos a descargar una página web e invocar contenido de ella. Este es el equivalente en Visual Basic script.

![el equivalente en Visual Basic script](images/AMSI6.png)

Lo que hace que las cosas empeoren en ambos ejemplos es que el motor antivirus inspecciona los archivos abiertos por el usuario. Si el contenido malintencionado solo se encuentra en la memoria, el ataque puede pasar desapercibido.

En esta sección se han mostrado las limitaciones de la detección mediante firmas tradicionales. Pero, aunque un script malintencionado puede pasar por varios pases de desuso, en última instancia debe proporcionar al motor de scripting código sin formato y sin ofuscar. Y en ese momento, como se describe en la primera sección anterior, los hosts de scripting integrados de Windows 10 llaman a las API de AMSI para solicitar un examen de este contenido no &mdash; &mdash; protegido. Y la aplicación puede hacer lo mismo.

## <a name="related-resources"></a>Recursos relacionados

* [Amenazas sin archivos](/windows/security/threat-protection/intelligence/fileless-threats)
* [Office VBA + AMSI: Parting the veil on malicious macros (VBA + AMSI: parting the veil on malicious macros) (VBA + AMSI: parting the veil on malicious](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/12/office-vba-amsi-parting-the-veil-on-malicious-macros/)
* [Fuera de la vista, pero no invisible: eliminación de malware sin archivos con supervisión de comportamiento, AMSI y AV de próxima generación](https://cloudblogs.microsoft.com/microsoftsecure/2018/09/27/out-of-sight-but-not-invisible-defeating-fileless-malware-with-behavior-monitoring-amsi-and-next-gen-av/)
