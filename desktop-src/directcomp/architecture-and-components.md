---
title: Arquitectura y componentes
description: En este tema se describen los componentes que componen Microsoft DirectComposition.
ms.assetid: 7C79B330-41EA-4BA0-9103-BB5A0C3D4CE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2de495aa170560b1e7082cacf1893a8c94905a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104078186"
---
# <a name="architecture-and-components"></a>Arquitectura y componentes

> [!NOTE]
> En el caso de las aplicaciones de Windows 10, se recomienda usar las API de Windows. UI. Composition en lugar de DirectComposition. Para obtener más información, consulte [modernice su aplicación de escritorio con el nivel de objetos visuales](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se describen los componentes que componen Microsoft DirectComposition. Consta de las siguientes secciones.

-   [Componentes de software](#software-components)
-   [Biblioteca de aplicaciones](#application-library)
-   [Motor de composición](#composition-engine)
-   [Temas relacionados](#related-topics)

## <a name="software-components"></a>Componentes de software

DirectComposition consta de los siguientes componentes de software principales.

-   Biblioteca de aplicaciones de modo de usuario (dcomp.dll) que implementa la API pública basada en el modelo de objetos componentes (COM).
-   Un motor de composición de modo de usuario (dwmcore.dll) que se hospeda en el proceso de Administrador de ventanas de escritorio (DWM) (dwm.exe) y realiza la composición de escritorio real.
-   Base de datos de objetos de modo kernel (parte de win32k.sys) que calcula las referencias de los comandos de la aplicación al motor de composición.

Una sola instancia del motor de composición controla los árboles de composición de DirectComposition para todas las aplicaciones y el árbol de composición de DWM, que representa todo el escritorio. Se crea una instancia de la base de datos de objetos de modo kernel y del motor de composición de modo de usuario una vez por sesión, por lo que una máquina Terminal Server con varios usuarios tiene varias instancias de ambos componentes.

En el diagrama siguiente se muestran los componentes principales de DirectComposition y cómo se relacionan entre sí.

![arquitectura de nivel superior de directcomposition](images/directcomposition-top-level-architecture.png)

## <a name="application-library"></a>Biblioteca de aplicaciones

La biblioteca de aplicaciones de DirectComposition es una API basada en COM pública con un único punto de entrada plano que se exporta desde dcomp.dll y devuelve un puntero de interfaz a un objeto de dispositivo. El objeto de dispositivo, a su vez, tiene métodos para crear todos los demás objetos, cada uno de los cuales se representa mediante un puntero de interfaz. Todas las interfaces DirectComposition heredan de y implementan completamente la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . Todos los métodos que aceptan interfaces DirectCompositions comprueban si la interfaz está implementada dentro de dcomp.dll o si está implementada por otro componente. Dado que DirectComposition no es extensible, los métodos que toman interfaces como parámetros devuelven E \_ INVALIDARG si las interfaces no se implementan en dcomp.dll. La API no requiere ningún privilegio especial; puede ser llamado por procesos que se ejecutan en el nivel más bajo de acceso. Sin embargo, dado que la API no funciona en la sesión 0, no es adecuada para los servicios. En estos aspectos, la API DirectComposition es similar a otras API de Microsoft DirectX, especialmente en Direct2D, Microsoft Direct3D y Microsoft DirectWrite.

Dado que el motor de composición está diseñado exclusivamente para la ejecución asincrónica, las propiedades de objeto de la API de DirectComposition son de solo escritura. Todas las propiedades tienen métodos de establecedor, pero no métodos de captador. Leer propiedades no solo es un uso intensivo de los recursos, sino que también puede ser inexacto porque cualquier valor devuelto por el motor de composición puede dejar de ser válido inmediatamente. Esto puede ocurrir si, por ejemplo, una animación independiente se enlaza a la propiedad que se está leyendo.

La API es segura para subprocesos. Una aplicación puede llamar a cualquier método desde cualquier subproceso en cualquier momento. Sin embargo, dado que se debe llamar a muchos métodos de API en una secuencia determinada, sin ninguna sincronización, una aplicación puede experimentar un comportamiento imprevisible en función de cómo intercalan los subprocesos. Por ejemplo, si dos subprocesos cambian la misma propiedad del mismo objeto a valores diferentes al mismo tiempo, la aplicación no puede predecir cuál de los dos valores será el valor final de la propiedad. Del mismo modo, si dos subprocesos llaman a [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) en el mismo dispositivo, ninguno de los subprocesos obtiene un comportamiento realmente transaccional porque una llamada a **commit** en un subproceso enviará el lote de todos los comandos emitidos por ambos subprocesos, no solo el que llamó a **commit**.

El sistema mantiene todo el estado interno por cada objeto de dispositivo. Si una aplicación crea dos o más objetos de dispositivo DirectComposition, la aplicación puede mantener lotes independientes y otro estado entre los dos.

Todos los objetos DirectComposition tienen afinidad de objeto de dispositivo; los objetos creados por un objeto de dispositivo determinado solo se pueden usar con ese objeto de dispositivo y solo pueden asociarse a otros objetos creados por el mismo objeto de dispositivo. En otras palabras, cada objeto de dispositivo es una isla separada independiente de la funcionalidad. La única excepción es la clase visual, que permite compilar árboles visuales en los que un objeto visual puede pertenecer a un objeto de dispositivo diferente al de su elemento primario. Esto permite escenarios en los que una aplicación y un control pueden administrar un único árbol de composición sin necesidad de compartir un único objeto de dispositivo DirectComposition.

## <a name="composition-engine"></a>Motor de composición

El motor de composición DirectComposition se ejecuta en un proceso dedicado, independiente de cualquier proceso de aplicación. Un único proceso de composición, dwm.exe, admite todas las aplicaciones de una sesión. Cada aplicación puede crear dos árboles visuales para cada ventana que posee. Todos los árboles se implementan realmente como subárboles de un árbol visual mayor que también abarca las estructuras de composición de DWM. DWM crea un árbol visual grande para cada escritorio de una sesión. Estas son las ventajas principales de esta arquitectura:

-   El motor de composición tiene acceso a todos los mapas de bits de la aplicación y a los árboles visuales, lo que permite la interoperabilidad y composición de ventanas entre procesos.
-   El motor de composición se ejecuta en un proceso del sistema de confianza que es independiente de cualquier proceso de aplicación, lo que permite que las aplicaciones que tienen derechos de acceso de acceso seguro compongan contenido protegido.
-   El motor de composición puede detectar si una ventana determinada es totalmente ocluidos y evita gastar recursos de CPU y de unidad de procesamiento de gráficos (GPU) compuestas para la ventana.
-   El motor de composición se puede componer directamente en el búfer de reserva de la pantalla, evitando la necesidad de una copia adicional necesaria para los motores de composición por proceso.
-   Todas las aplicaciones comparten un único dispositivo de Direct3D para la composición, lo que ofrece un ahorro de memoria considerable.

El árbol visual es una estructura retenida. La API de DirectComposition expone métodos para editar la estructura en lotes de cambios que se procesan de forma atómica. El objeto raíz de la API DirectComposition es el objeto de dispositivo, que actúa como generador para todos los demás objetos DirectComposition y contiene un método denominado [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). El motor de composición no refleja los cambios que la aplicación realiza en el árbol visual hasta que la aplicación llame a **commit**, momento en el cual todos los cambios desde la última **confirmación** se procesan como una sola transacción.

El requisito de llamar a [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) es similar al concepto de "Frame", salvo que, dado que el motor de composición se ejecuta de forma asincrónica, puede presentar varios marcos diferentes entre las llamadas a **commit**. En DirectComposition, un *marco* es una sola iteración del motor de composición y el intervalo empleado por una aplicación entre dos llamadas a **commit** se denomina *lote*.

DirectComposition procesa por lotes todas las llamadas a la aplicación a la API de DirectComposition. La base de datos de objetos de kernel, que se implementa en el controlador de sesión win32k.sys, almacena toda la información de estado asociada a las llamadas API.

El motor de composición produce un fotograma por cada espacio en blanco vertical en la pantalla. El marco se inicia en un espacio en blanco vertical y tiene como destino el siguiente espacio en blanco vertical. Cuando se inicia el fotograma, el motor de composición recoge todos los lotes pendientes e incluye sus comandos en ese marco. Los lotes se colocan en una cola pendiente cuando la aplicación llama a [**commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)y la cola pendiente se vacía atómicamente al principio del marco. Por lo tanto, hay un único punto en el tiempo que marca el principio de un marco. Los lotes enviados antes de este punto se incluyen en el marco, mientras que los lotes enviados después de deben esperar hasta el siguiente fotograma que se va a procesar. El bucle de composición completo es el siguiente:

1.  Estima la hora del siguiente espacio en blanco vertical.
2.  Recupere todos los lotes pendientes.
3.  Procesa los lotes recuperados.
4.  Actualice todas las animaciones con el tiempo estimado en el paso 1.
5.  Determine las regiones de la pantalla que deben volver a componerse.
6.  Vuelva a crear las regiones desfasadas.
7.  Presente el fotograma volteando los búferes de atrás y front para cada pantalla.
8.  Si no se ha compuesto nada y se presentó en los pasos 6 y 7, espere a que se confirme un lote.
9.  Espere al siguiente espacio en blanco vertical.

Si hay varios monitores conectados a un único adaptador de vídeo, el motor de composición utiliza el espacio en blanco vertical del monitor principal para controlar el bucle de composición y establecer los tiempos de muestreo de la animación. Cada monitor se representa mediante una cadena de volteo de pantalla completa independiente; el motor de composición repite los pasos 6 y 7 para cada monitor, en modo Round-Robin, con un solo dispositivo Direct3D. Si también hay varios adaptadores de vídeo, el motor de composición usa un dispositivo Direct3D independiente para cada adaptador de vídeo en los pasos 6 y 7.

Los fotogramas de composición están programados para iniciarse siempre en un espacio en blanco vertical, como se muestra en la ilustración siguiente.

![programación de fotogramas de composición](images/composition-frame-scheduling.png)

Si el motor de composición no realiza ningún trabajo porque el árbol de composición no ha cambiado, el subproceso de composición entra en suspensión mientras se espera un nuevo lote. Cuando se envía un nuevo lote, el subproceso de composición se activa, pero vuelve inmediatamente a la suspensión hasta el siguiente espacio en blanco vertical. Este comportamiento garantiza horas de inicio y finalización de fotogramas predecibles para las aplicaciones y para el motor de composición.

El motor de composición publica los tiempos de presentación de los fotogramas y la velocidad de fotogramas actual. La publicación de esta información permite a las aplicaciones calcular el tiempo de presentación de sus propios lotes, lo que a su vez permite sincronizar las animaciones. En concreto, una aplicación puede utilizar una combinación de estadísticas de fotogramas del motor de composición y un modelo histórico de cuánto tiempo tarda su subproceso de interfaz de usuario en generar un lote, para determinar el tiempo de muestreo de sus propias animaciones.

Por ejemplo, al principio del lote de aplicaciones que se muestra en la ilustración anterior, la aplicación puede consultar el motor de composición para determinar el tiempo exacto de presentación del fotograma siguiente. A continuación, la aplicación puede usar la hora actual, junto con información sobre los lotes anteriores que ha generado, para determinar si la aplicación puede completar el lote actual antes del siguiente espacio en blanco vertical. Por lo tanto, la aplicación utiliza el tiempo de presentación del marco como el tiempo de muestreo para sus propias animaciones. Si la aplicación determina que es improbable que complete su trabajo en el espacio en blanco vertical actual, la aplicación puede usar la hora del fotograma posterior como el tiempo de muestreo, usando la información de velocidad de fotogramas devuelta por el motor de composición para calcular ese tiempo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 