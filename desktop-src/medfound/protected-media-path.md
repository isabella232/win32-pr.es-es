---
description: 'En este tema se describen tres temas interrelacionados: entorno protegido, puerta de enlace de interoperabilidad multimedia y revocación y renovación.'
ms.assetid: e88806ae-0041-4b4a-a8df-69718a651e82
title: Ruta de acceso a medios protegidos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7304edadf1623d41bc2f1f5c6b2b4cda2dd5f598
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/03/2021
ms.locfileid: "104557749"
---
# <a name="protected-media-path"></a>Ruta de acceso a medios protegidos

En este tema se describen tres temas interrelacionados: entorno protegido, puerta de enlace de interoperabilidad multimedia y revocación y renovación.

-   Un entorno protegido (PE) es un conjunto de tecnologías que permite que el contenido protegido fluya desde y hasta a través de Windows Vista de manera protegida. Todos los componentes de dentro de un entorno protegido son de confianza y el proceso está protegido contra la manipulación.
-   La ruta de acceso a medios protegidos (PMP) es un archivo ejecutable que se ejecuta en un entorno protegido.
-   Si un componente de confianza en el PE se pone en peligro, después del proceso de vencimiento, se revocará. Sin embargo, Microsoft proporciona un mecanismo de renovación para instalar una versión de confianza más reciente del componente cuando está disponible.

Para obtener información acerca de los componentes multimedia protegidos de la firma de código, consulte las notas del producto [firma de código para componentes multimedia protegidos en Windows Vista](/windows-hardware/test/hlk/).

Este tema contiene las siguientes secciones:

-   [Entorno protegido](#protected-environment)
-   [Diseño del entorno protegido](#design-of-the-protected-environment)
-   [Ruta de acceso a medios protegidos](#protected-media-path)
    -   [Entidades de confianza de entrada](#input-trust-authorities)
    -   [Entidades de confianza de salida](#output-trust-authorities)
    -   [Objetos de Directiva](#policy-objects)
    -   [Crear objetos en el PMP](#creating-objects-in-the-pmp)
-   [Información general sobre la negociación de directivas](#overview-of-policy-negotiation)
-   [Revocación y renovación](#revocation-and-renewal)
-   [Protección de vínculo de salida](#output-link-protection)
-   [Temas relacionados](#related-topics)

## <a name="protected-environment"></a>Entorno protegido

La protección de contenido abarca varias tecnologías, cada una de las cuales intenta asegurarse de que el contenido no se puede usar de forma que sea incoherente con el intento del propietario o del proveedor de contenido. Estas tecnologías incluyen la protección contra copia, la protección de vínculos, el acceso condicional y la administración de derechos digitales (DRM). La base de cada es una relación de confianza: el acceso al contenido solo se concede a los componentes de software que se adhieren a los términos de uso asignados a ese contenido.

Para minimizar las amenazas contra contenido protegido, Windows Vista y el software Media Foundation permiten que el código de confianza se ejecute en un entorno protegido. Un PE es un conjunto de componentes, directrices y herramientas diseñados para aumentar la protección contra la piratería de contenido.

Antes de examinar el PE más detenidamente, es importante comprender las amenazas que está diseñada para minimizar. Supongamos que está ejecutando una aplicación multimedia en un proceso de modo de usuario. La aplicación está vinculada a las diversas bibliotecas de vínculos dinámicos (dll) que contienen complementos multimedia, como descodificadores. Otros procesos también se ejecutan en modo de usuario y se cargan varios controladores en el kernel. Si no se implementa ningún mecanismo de confianza, existen las siguientes amenazas:

-   La aplicación puede tener acceso a los medios protegidos directamente o a piratear la memoria de proceso.
-   Los complementos pueden tener acceso al contenido directamente o atacar la memoria del proceso.
-   Otros procesos pueden atacar la memoria del proceso multimedia directamente o mediante la inserción de código.
-   Los controladores de kernel pueden atacar la memoria de proceso multimedia.
-   El contenido se puede enviar fuera del sistema a través de un medio desprotegido. (La protección de vínculos está diseñada para mitigar esta amenaza).

## <a name="design-of-the-protected-environment"></a>Diseño del entorno protegido

Un entorno protegido se ejecuta en un proceso protegido independiente de la aplicación multimedia. La característica de proceso protegido de Windows Vista impide que otros procesos tengan acceso al proceso protegido.

Cuando se crea un proceso protegido, los componentes principales del kernel identifican los componentes y complementos que no son de confianza para que el entorno protegido pueda negar su carga. Un componente de confianza es aquél que Microsoft ha firmado correctamente. El kernel también realiza el seguimiento de los módulos que se cargan en él, lo que permite que el entorno protegido detenga la reproducción del contenido protegido si se carga un módulo que no es de confianza. Antes de cargar un componente de kernel, el kernel comprueba para determinar si es de confianza. Si no es así, los componentes de confianza que ya están en el PE rechazan el contenido protegido. Para habilitar esto, los componentes de PE realizan periódicamente un protocolo de enlace protegido criptográficamente con el kernel. Si hay un componente de modo kernel que no es de confianza, se produce un error en el protocolo de enlace y indica al PE que hay un componente que no es de confianza.

Si un componente de confianza se pone en peligro, se puede revocar después del proceso de vencimiento. Microsoft proporciona un mecanismo de renovación para instalar una versión de confianza más reciente cuando esté disponible.

## <a name="protected-media-path"></a>Ruta de acceso a medios protegidos

La ruta de acceso a medios protegidos (PMP) es el ejecutable principal de PE para Media Foundation. El PMP es extensible, de modo que se pueden admitir mecanismos de protección de contenido de terceros.

El PMP acepta contenido protegido y directivas asociadas de cualquier origen de Media Foundation mediante cualquier sistema de protección de contenido, incluidos los que proporcionan terceros. Envía contenido a cualquier receptor de Media Foundation, siempre y cuando el receptor cumpla las directivas especificadas por el origen. También admite transformaciones entre el origen y el receptor, incluidas las transformaciones de terceros, siempre y cuando sean de confianza.

El PMP se ejecuta en un proceso protegido aislado de la aplicación multimedia. La aplicación solo tiene la capacidad de intercambiar mensajes de comando y control con el PMP, pero no tiene acceso al contenido después de pasarlo a la PMP. En el siguiente diagrama se muestra este proceso.

![diagrama de la ruta de acceso a los medios protegidos](images/pmp04.png)

Los cuadros sombreados representan componentes que pueden ser proporcionados por terceros. Todos los componentes creados en el proceso protegido deben estar firmados y son de confianza.

La aplicación crea una instancia de la sesión multimedia dentro del proceso protegido y recibe un puntero a una sesión multimedia del proxy, que calcula las referencias de los punteros de interfaz en el límite del proceso.

El origen de medios se puede crear en el proceso de la aplicación, como se muestra aquí, o dentro del proceso protegido. Si el origen de medios se crea dentro del proceso de la aplicación, el origen crea un proxy para sí mismo en el proceso protegido.

Todos los demás componentes de canalización, como descodificadores y receptores de medios, se crean en el proceso protegido. Si estos objetos exponen cualquier interfaz personalizada para las aplicaciones, deben proporcionar un proxy o código auxiliar DCOM para calcular las referencias de la interfaz.

Para aplicar la Directiva en el contenido protegido a medida que fluye a través de la canalización, el PMP usa tres tipos de componentes: entidades de confianza de entrada (ITAs), entidades de confianza de salida (OTAs) y objetos de directiva. Estos componentes funcionan juntos para conceder o restringir derechos para usar el contenido, y para especificar las protecciones del vínculo que se deben emplear al reproducir contenido, como Content Protection digital de ancho de banda alto (HDCP).

### <a name="input-trust-authorities"></a>Entidades de confianza de entrada

Un origen de medios de confianza crea una ITA y realiza varias funciones:

-   Especifica los derechos para usar el contenido. Los derechos pueden incluir el derecho a reproducir contenido, transferirlo a un dispositivo, etc. Define una lista ordenada de sistemas de protección de salida aprobados y las directivas de salida correspondientes para cada sistema. La ITA almacena esta información en un objeto de directiva.
-   Proporciona el descifrador necesario para descifrar el contenido.
-   Establece la confianza con el módulo kernel en el entorno protegido para asegurarse de que la ITA se ejecuta dentro de un entorno de confianza.

Una ITA está asociada a un flujo individual que contiene contenido protegido. Un flujo solo puede tener una ITA y una instancia de ITA solo se puede asociar a una secuencia.

### <a name="output-trust-authorities"></a>Entidades de confianza de salida

Un OTA está asociado a una salida de confianza. La OTA expone una acción que la salida de confianza puede realizar en el contenido, como reproducir o copiar. Su rol es aplicar uno o varios sistemas de protección de salida requeridos por la ITA. La OTA consulta el objeto de directiva proporcionado por ITA para determinar qué sistema de protección debe aplicar.

### <a name="policy-objects"></a>Objetos de Directiva

Un objeto de directiva encapsula los requisitos de protección de contenido de una ITA. Lo usa el motor de directivas para negociar la compatibilidad de la protección de contenido con una OTA. OTAs los objetos de directiva de consulta para determinar los sistemas de protección que deben aplicar en cada salida del contenido actual.

### <a name="creating-objects-in-the-pmp"></a>Crear objetos en el PMP

Para crear un objeto en la ruta de acceso a medios protegidos (PMP), [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) llama a [**IMFPMPHostApp:: ActivateClassById**](/windows/desktop/api/mfidl/nf-mfidl-imfpmphostapp-activateclassbyid), con el formato **IStream** de entrada especificado de la siguiente manera:

``` syntax
Format: (All DWORD values are serialized in little-endian order)
[GUID (content protection system guid, obtained from Windows.Media.Protection.MediaProtectionSystemId)]
[DWORD (track count, use the actual track count even if all tracks are encrypted using the same data, note that zero is invalid)]
[DWORD (next track ID, use -1 if all remaining tracks are encrypted using the same data)]
[DWORD (next track's binary data size)]
[BYTE* (next track's binary data)]
{ Repeat from "next track ID" above for each stream }
```

## <a name="overview-of-policy-negotiation"></a>Información general sobre la negociación de directivas

Hay tres requisitos fundamentales que deben cumplirse antes de que se pueda procesar el contenido protegido en el PMP. En primer lugar, solo se debe enviar contenido protegido a salidas de confianza. En segundo lugar, solo se deben aplicar las acciones permitidas a un flujo. En tercer lugar, solo se deben usar los sistemas de protección de salida aprobados para reproducir un flujo. El motor de directivas coordina entre ITAs y OTAs para asegurarse de que se cumplen estos requisitos.

La forma más fácil de entender el proceso es recorrer un ejemplo simplificado que identifica los pasos necesarios para reproducir contenido de formato de sistema avanzado (ASF) protegido por Rights Management digital (WMDRM) de Windows Media.

Cuando un usuario inicia una aplicación de reproducción y abre un archivo ASF que tiene una secuencia de audio protegida y una secuencia de vídeo protegida, se deben realizar los siguientes pasos:

1.  La aplicación crea el origen de medios ASF y la sesión de la ruta de acceso a medios protegidos (PMP). Media Foundation crea un proceso de PMP.
2.  La aplicación crea una topología parcial que contiene un nodo de origen de audio conectado al representador de audio y un nodo de origen de vídeo conectado al representador de vídeo mejorado (EVR). En el caso de los representadores, la aplicación no crea directamente el representador. En su lugar, la aplicación crea en el proceso sin protección un objeto conocido como *objeto de activación*. El PMP usa el objeto de activación para crear los representadores en el proceso protegido. (Para obtener más información sobre los objetos de activación, vea [objetos de activación](activation-objects.md)).
3.  La aplicación establece la topología parcial en la sesión de PMP.
4.  La sesión de PMP serializa la topología y la pasa al host de PMP en el proceso protegido. El host de PMP envía la topología al motor de directivas.
5.  El cargador de topología llama a [**IMFInputTrustAuthority:: GetDecrypter**](/windows/desktop/api/mfidl/nf-mfidl-imfinputtrustauthority-getdecrypter) en el itas e inserta los descifradores en la topología inmediatamente inferior de los nodos de origen correspondientes.
6.  El cargador de topología inserta los descodificadores de audio y vídeo de nivel inferior de los nodos de Decrypter.
7.  El motor de directivas examina los nodos insertados para determinar si alguno implementa la interfaz [**IMFTrustedOutput**](/windows/desktop/api/mfidl/nn-mfidl-imftrustedoutput) . Los EVR y el representador de audio implementan **IMFTrustedOutput**, ya que envían datos fuera de la PMP.
8.  Cada ITA confirma que se ejecuta dentro de un proceso protegido mediante la realización de un protocolo de enlace criptográfico con un módulo de kernel de entorno protegido.
9.  Para cada flujo, el motor de directivas negocia la Directiva obteniendo un objeto de directiva de la ITA y pasándolo a la OTA. La OTA proporciona una lista de los sistemas de protección que admite y el objeto de directiva indica qué sistemas de protección deben aplicarse, junto con la configuración correcta. Después, la OTA aplica esta configuración. Si no puede hacerlo, el contenido se bloquea.

## <a name="revocation-and-renewal"></a>Revocación y renovación

Un componente de confianza se puede revocar si se pone en peligro o se detecta que infringe los contratos de licencia en los que se confía inicialmente. Existe un mecanismo de renovación para instalar una versión más reciente y de mayor confianza del componente.

Los componentes de confianza se firman con un certificado criptográfico. Microsoft publica una lista de revocación global (GRL) que identifica los componentes que se han revocado. El GRL está firmado digitalmente para garantizar su autenticidad. Los propietarios de contenido pueden garantizar, a través del mecanismo de la Directiva, que la versión actual del GRL está presente en el equipo del usuario.

## <a name="output-link-protection"></a>Protección de vínculo de salida

Cuando se ve el contenido de vídeo Premium, los fotogramas descifrados descomprimidos viajan a través de un conector físico al dispositivo de pantalla. Los proveedores de contenido pueden requerir que los fotogramas de vídeo estén protegidos en este punto, a medida que viajan por el conector físico. Existen varios mecanismos de protección para este propósito, como High-Bandwidth Digital Content Protection (HDCP) y DisplayPort Content Protection (DPCP). La transmisión por video con la transmisión por vídeo se aplica a estas protecciones mediante el [Administrador de protección de salida](output-protection-manager.md) (OPM). El administrador de protección de salida envía comandos al controlador de gráficos y el controlador de gráficos exige cualquier mecanismo de protección de vínculos que requiera la Directiva.

![un diagrama que muestra la relación entre el vídeo OTA y OPM.](images/pmp05.png)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de Media Foundation](about-the-media-foundation-sdk.md)
</dt> <dt>

[Arquitectura de Media Foundation](media-foundation-architecture.md)
</dt> <dt>

[Content Protection basados en GPU](gpu-based-content-protection.md)
</dt> <dt>

[Administrador de protección de salida](output-protection-manager.md)
</dt> <dt>

[Sesión de medios de PMP](pmp-media-session.md)
</dt> </dl>

 

 
