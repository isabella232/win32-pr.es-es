---
description: 'En este tema se tratan tres temas interrelacionados: entorno protegido, puerta de enlace de interoperabilidad de medios y revocación y renovación.'
ms.assetid: e88806ae-0041-4b4a-a8df-69718a651e82
title: Ruta de acceso multimedia protegida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ebb2b22e6ad887134f91e93b43a698afdef0ebc36e1521d70e5e17fefedd8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035036"
---
# <a name="protected-media-path"></a>Ruta de acceso multimedia protegida

En este tema se tratan tres temas interrelacionados: entorno protegido, puerta de enlace de interoperabilidad de medios y revocación y renovación.

-   Un entorno protegido (PE) es un conjunto de tecnologías que permite que el contenido protegido fluya desde y Windows Vista de forma protegida. Todos los componentes dentro de un entorno protegido son de confianza y el proceso está protegido contra la manipulación.
-   La ruta de acceso multimedia protegida (PMP) es un archivo ejecutable que se ejecuta en un entorno protegido.
-   Si un componente de confianza del PE se ve comprometido, después del debido proceso se revocará. Sin embargo, Microsoft proporciona un mecanismo de renovación para instalar una versión de confianza más reciente del componente cuando esté disponible.

Para obtener información sobre la firma de código de componentes multimedia protegidos, vea las white [paper Code Signing for Protected Media Components in Windows Vista](/windows-hardware/test/hlk/).

Este tema contiene las siguientes secciones:

-   [Entorno protegido](#protected-environment)
-   [Diseño del entorno protegido](#design-of-the-protected-environment)
-   [Ruta de acceso multimedia protegida](#protected-media-path)
    -   [Entidades de confianza de entrada](#input-trust-authorities)
    -   [Autoridades de confianza de salida](#output-trust-authorities)
    -   [Objetos de directiva](#policy-objects)
    -   [Crear objetos en el PMP](#creating-objects-in-the-pmp)
-   [Introducción a la negociación de directivas](#overview-of-policy-negotiation)
-   [Revocación y renovación](#revocation-and-renewal)
-   [Protección de vínculos de salida](#output-link-protection)
-   [Temas relacionados](#related-topics)

## <a name="protected-environment"></a>Entorno protegido

La protección de contenido abarca varias tecnologías, cada una de las cuales intenta asegurarse de que el contenido no se puede usar de forma incoherente con la intención del propietario o proveedor del contenido. Estas tecnologías incluyen la protección de copia, la protección de vínculos, el acceso condicional y la administración de derechos digitales (DRM). La base de cada uno es la confianza: el acceso al contenido solo se concede a los componentes de software que cumplen los términos de uso asignados a ese contenido.

Para minimizar las amenazas contra el contenido protegido, Windows Vista y Media Foundation Software permiten que el código de confianza se ejecute en un entorno protegido. Un PE es un conjunto de componentes, directrices y herramientas diseñados para aumentar la protección contra la piratería de contenido.

Antes de examinar más de cerca el PE, es importante comprender las amenazas que está diseñada para minimizar. Supongamos que está ejecutando una aplicación multimedia en un proceso en modo de usuario. La aplicación está vinculada a las distintas bibliotecas de vínculos dinámicos (DLL) que contienen complementos multimedia, como descodificadores. Otros procesos también se ejecutan en modo de usuario y se cargan varios controladores en el kernel. Si no hay ningún mecanismo de confianza, existen las siguientes amenazas:

-   La aplicación puede acceder directamente a los medios protegidos o hackear la memoria del proceso.
-   Los complementos pueden acceder al contenido directamente o piratear la memoria del proceso.
-   Otros procesos pueden hackear la memoria del proceso multimedia directamente o mediante la inyección de código.
-   Los controladores de kernel pueden piratear la memoria del proceso multimedia.
-   El contenido se puede enviar fuera del sistema a través de un medio no protegido. (La protección de vínculos está diseñada para mitigar esta amenaza).

## <a name="design-of-the-protected-environment"></a>Diseño del entorno protegido

Un entorno protegido se ejecuta en un proceso protegido independiente de la aplicación multimedia. La característica de proceso protegido de Windows Vista impide que otros procesos accedan al proceso protegido.

Cuando se crea un proceso protegido, los componentes principales del kernel identifican componentes y complementos que no son de confianza para que el entorno protegido pueda rechazar su carga. Un componente de confianza es aquel que Microsoft ha firmado correctamente. El kernel también realiza un seguimiento de los módulos que se cargan en él, lo que permite que el entorno protegido detenga la reproducción de contenido protegido si se carga un módulo que no es de confianza. Antes de cargar un componente de kernel, el kernel comprueba si es de confianza. Si no es así, los componentes de confianza que ya están en el PE rechazan procesar el contenido protegido. Para habilitar esto, los componentes de PE realizan periódicamente un protocolo de enlace protegido criptográficamente con el kernel. Si hay un componente de modo kernel que no es de confianza, se produce un error en el protocolo de enlace e indica al PE que existe un componente que no es de confianza.

Si un componente de confianza se ve comprometido, después del debido proceso se puede revocar. Microsoft proporciona un mecanismo de renovación para instalar una versión de confianza más reciente cuando esté disponible.

## <a name="protected-media-path"></a>Ruta de acceso multimedia protegida

La ruta de acceso multimedia protegida (PMP) es el ejecutable pe principal para Media Foundation. El PMP es extensible, por lo que se pueden admiten mecanismos de protección de contenido de terceros.

El PMP acepta contenido protegido y directivas asociadas de cualquier origen de Media Foundation mediante cualquier sistema de protección de contenido, incluidos los proporcionados por terceros. Envía contenido a cualquier receptor Media Foundation, siempre que el receptor cumpla las directivas especificadas por el origen. También admite transformaciones entre el origen y el receptor, incluidas las transformaciones de terceros, siempre que sean de confianza.

El PMP se ejecuta en un proceso protegido aislado de la aplicación multimedia. La aplicación solo tiene la capacidad de intercambiar mensajes de comando y control con el PMP, pero no tiene acceso al contenido después de pasarlo al PMP. En el siguiente diagrama se muestra este proceso.

![diagrama de la ruta de acceso multimedia protegida](images/pmp04.png)

Los cuadros sombreados representan componentes que pueden proporcionar terceros. Todos los componentes creados dentro del proceso protegido deben estar firmados y de confianza.

La aplicación crea una instancia de la sesión multimedia dentro del proceso protegido y recibe un puntero a una sesión multimedia de proxy, que serializa los punteros de interfaz a través del límite del proceso.

El origen de medios se puede crear dentro del proceso de aplicación, como se muestra aquí, o dentro del proceso protegido. Si el origen multimedia se crea dentro del proceso de aplicación, el origen crea un proxy para sí mismo en el proceso protegido.

Todos los demás componentes de canalización, como descodificadores y receptores multimedia, se crean en el proceso protegido. Si estos objetos exponen interfaces personalizadas para aplicaciones, deben proporcionar un proxy/código auxiliar DCOM para serializar la interfaz.

Para aplicar la directiva en el contenido protegido a medida que fluye a través de la canalización, el PMP usa tres tipos de componentes: entidades de confianza de entrada (ITA), entidades de confianza de salida (ATA) y objetos de directiva. Estos componentes funcionan conjuntamente para conceder o restringir los derechos de uso del contenido y para especificar las protecciones de vínculo que se deben emplear al reproducir contenido, como La aplicación digital de ancho de banda alto Content Protection (HDCP).

### <a name="input-trust-authorities"></a>Entidades de confianza de entrada

Un ITA se crea mediante un origen multimedia de confianza y realiza varias funciones:

-   Especifica los derechos para usar el contenido. Los derechos pueden incluir el derecho a reproducir contenido, transferirlo a un dispositivo, y así sucesivamente. Define una lista ordenada de sistemas de protección de salida aprobados y las directivas de salida correspondientes para cada sistema. El ITA almacena esta información en un objeto de directiva.
-   Proporciona el descifrador necesario para descifrar el contenido.
-   Establece la confianza con el módulo kernel en el entorno protegido para asegurarse de que el ITA se ejecuta dentro de un entorno de confianza.

Un ITA está asociado a una secuencia individual que contiene contenido protegido. Una secuencia solo puede tener un ITA y una instancia de un ITA solo se puede asociar a una secuencia.

### <a name="output-trust-authorities"></a>Autoridades de confianza de salida

Un OTA está asociado a una salida de confianza. El OTA expone una acción que la salida de confianza puede realizar en el contenido, como la reproducción o la copia. Su rol es aplicar uno o varios sistemas de protección de salida necesarios para el ITA. El OTA consulta el objeto de directiva proporcionado por ITA para determinar qué sistema de protección debe aplicar.

### <a name="policy-objects"></a>Objetos de directiva

Un objeto de directiva encapsula los requisitos de protección de contenido de un ITA. Lo usa el motor de directivas para negociar la compatibilidad con la protección de contenido con un OTA. Las ATA consultan objetos de directiva para determinar qué sistemas de protección deben aplicar en cada salida del contenido actual.

### <a name="creating-objects-in-the-pmp"></a>Crear objetos en el PMP

Para crear un objeto en la ruta de acceso de medios protegidos (PMP), EL MÉTODO DE LA RUTA DE ACCESO (PMP) llama a [**LAFUSPMPHostApp::ActivateClassById**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-activateclassbyid), con el formato **IStream** de entrada especificado de la siguiente manera: [](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)

``` syntax
Format: (All DWORD values are serialized in little-endian order)
[GUID (content protection system guid, obtained from Windows.Media.Protection.MediaProtectionSystemId)]
[DWORD (track count, use the actual track count even if all tracks are encrypted using the same data, note that zero is invalid)]
[DWORD (next track ID, use -1 if all remaining tracks are encrypted using the same data)]
[DWORD (next track's binary data size)]
[BYTE* (next track's binary data)]
{ Repeat from "next track ID" above for each stream }
```

## <a name="overview-of-policy-negotiation"></a>Introducción a la negociación de directivas

Hay tres requisitos fundamentales que deben cumplirse antes de que el contenido protegido se pueda procesar en el PMP. En primer lugar, el contenido protegido solo debe enviarse a salidas de confianza. En segundo lugar, solo las acciones permitidas se deben aplicar a una secuencia. En tercer lugar, solo se deben usar sistemas de protección de salida aprobados para reproducir una secuencia. El motor de directivas se coordina entre las ATA y las ATA para asegurarse de que se cumplen estos requisitos.

La manera más fácil de comprender el proceso es recorrer un ejemplo simplificado que identifica los pasos necesarios para reproducir contenido de formato de sistema avanzado (ASF) protegido por Windows Media Digital Rights Management (WMDRM).

Cuando un usuario inicia una aplicación de reproductor y abre un archivo ASF que tiene una secuencia de audio protegida y una secuencia de vídeo protegida, se deben realizar los pasos siguientes:

1.  La aplicación crea el origen de medios de ASF y la sesión de ruta de acceso multimedia protegida (PMP). Media Foundation crea un proceso PMP.
2.  La aplicación crea una topología parcial que contiene un nodo de origen de audio conectado al representador de audio y un nodo de origen de vídeo conectado al representador de vídeo mejorado (EVR). Para los representadores, la aplicación no crea directamente el representador. En su lugar, la aplicación crea en el proceso desprotegido un objeto conocido como objeto *de activación*. El PMP usa el objeto de activación para crear los representadores en el proceso protegido. (Para obtener más información sobre los objetos de activación, vea [Objetos de activación).](activation-objects.md)
3.  La aplicación establece la topología parcial en la sesión de PMP.
4.  La sesión de PMP serializa la topología y la pasa al host PMP en el proceso protegido. El host PMP envía la topología al motor de directivas.
5.  El cargador de topologías llama [**a CRYPTOInputTrustAuthority::GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) en los ITA e inserta los descifradores en la topología inmediatamente inferior de los nodos de origen correspondientes.
6.  El cargador de topologías inserta los descodificadores de audio y vídeo en la bajada de los nodos descifradores.
7.  El motor de directivas examina los nodos insertados para determinar si algún implemente la interfaz [**IMFTrustedOutput.**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput) El EVR y el representador de audio implementan **LAPPtrustedOutput**, ya que envían datos fuera del PMP.
8.  Cada ITA confirma que se ejecuta dentro de un proceso protegido mediante la realización de un protocolo de enlace criptográfico con un módulo de kernel de entorno protegido.
9.  Para cada secuencia, el motor de directivas negocia la directiva al obtener un objeto de directiva del ITA y pasarlo al OTA. El OTA proporciona una lista de los sistemas de protección que admite, y el objeto de directiva indica qué sistemas de protección se deben aplicar, junto con la configuración correcta. A continuación, el OTA aplica esta configuración. Si no puede hacerlo, el contenido se bloquea.

## <a name="revocation-and-renewal"></a>Revocación y renovación

Se puede revocar un componente de confianza si se pone en peligro o se detecta que infringe los contratos de licencia en los que se confió inicialmente. Existe un mecanismo de renovación para instalar una versión más reciente y de mayor confianza del componente.

Los componentes de confianza se firman mediante un certificado criptográfico. Microsoft publica una lista de revocación global (GRL) que identifica los componentes que se han revocado. La GRL está firmada digitalmente para garantizar su autenticidad. Los propietarios de contenido pueden asegurarse, a través del mecanismo de directiva, de que la versión actual de la GRL está presente en el equipo del usuario.

## <a name="output-link-protection"></a>Protección de vínculos de salida

Cuando se ve el contenido de vídeo premium, los fotogramas descifrados y sin comprimir viajan a través de un conector físico al dispositivo de visualización. Los proveedores de contenido pueden requerir que los fotogramas de vídeo estén protegidos en este momento, ya que viajan a través del conector físico. Existen varios mecanismos de protección para este propósito, incluidos High-Bandwidth Digital Content Protection (HDCP) y DisplayPort Content Protection (DPCP). El vídeo OTA aplica estas protecciones mediante el Administrador [de protección de salida](output-protection-manager.md) (OPM). El Administrador de protección de salida envía comandos al controlador de gráficos y el controlador de gráficos aplica los mecanismos de protección de vínculos que requiere la directiva.

![diagrama que muestra la relación entre el vídeo ota y opm.](images/pmp05.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Datos basados en GPU Content Protection](gpu-based-content-protection.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> <dt>

[Sesión multimedia de PMP](pmp-media-session.md)
</dt> </dl>

 

 
