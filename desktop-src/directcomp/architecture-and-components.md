---
title: Arquitectura y componentes
description: En este tema se describen los componentes que forma parte de Microsoft DirectComposition.
ms.assetid: 7C79B330-41EA-4BA0-9103-BB5A0C3D4CE2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb2de495aa170560b1e7082cacf1893a8c94905a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970428"
---
# <a name="architecture-and-components"></a>Arquitectura y componentes

> [!NOTE]
> Para las aplicaciones de Windows 10, se recomienda usar Windows.UI.Composition API en lugar de DirectComposition. Para obtener más información, [consulte Modernización de la aplicación de escritorio mediante la capa visual](/windows/uwp/composition/visual-layer-in-desktop-apps).

En este tema se describen los componentes que forma parte de Microsoft DirectComposition. Consta de las secciones siguientes.

-   [Componentes de software](#software-components)
-   [Biblioteca de aplicaciones](#application-library)
-   [Motor de composición](#composition-engine)
-   [Temas relacionados](#related-topics)

## <a name="software-components"></a>Componentes de software

DirectComposition consta de los siguientes componentes de software principales.

-   Una biblioteca de aplicaciones en modo de usuario (dcomp.dll) que implementa la API pública basada en Component Object Model (COM).
-   Un motor de composición en modo de usuario (dwmcore.dll) que se hospeda en el proceso de Administrador de ventanas de escritorio (DWM) (dwm.exe) y realiza la composición real del escritorio.
-   Una base de datos de objetos en modo kernel (parte de win32k.sys) que serializa los comandos de la aplicación al motor de composición.

Una sola instancia del motor de composición controla los árboles de composición de DirectComposition para todas las aplicaciones y el árbol de composición dwm, que representa todo el escritorio. Tanto la base de datos de objetos en modo kernel como el motor de composición en modo de usuario se crea una instancia una vez por sesión, por lo que una máquina de Terminal Server con varios usuarios tiene varias instancias de ambos componentes.

En el diagrama siguiente se muestran los componentes principales de DirectComposition y cómo se relacionan entre sí.

![arquitectura de nivel superior de directcomposition](images/directcomposition-top-level-architecture.png)

## <a name="application-library"></a>Biblioteca de aplicaciones

La biblioteca de aplicaciones DirectComposition es una API pública basada en COM con un único punto de entrada plano que se exporta desde dcomp.dll y devuelve un puntero de interfaz a un objeto de dispositivo. A su vez, el objeto de dispositivo tiene métodos para crear todos los demás objetos, cada uno de los cuales se representa mediante un puntero de interfaz. Todas las interfaces de DirectComposition heredan de e implementan completamente [**la interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) Todos los métodos que aceptan interfaces DirectComposition comprueban si la interfaz se implementa dentro de dcomp.dll o si la implementa otro componente. Dado que DirectComposition no es extensible, los métodos que toman interfaces como parámetros devuelven E INVALIDARG si las interfaces no se \_ implementan en dcomp.dll. La API no requiere privilegios especiales; Se puede llamar mediante procesos que se ejecutan en el nivel más bajo de acceso. Sin embargo, dado que la API no funciona en la sesión 0, no es adecuada para los servicios. En estos aspectos, DirectComposition API es similar a otras API de Microsoft DirectX, especialmente Direct2D, Microsoft Direct3D y Microsoft DirectWrite.

Dado que el motor de composición está diseñado exclusivamente para la ejecución asincrónica, las propiedades de objeto de DirectComposition API son de solo escritura. Todas las propiedades tienen métodos de establecimiento, pero no métodos de getter. La lectura de propiedades no solo consume muchos recursos, sino que también puede ser inexacta porque cualquier valor devuelto por el motor de composición puede convertirse inmediatamente en no válido. Esto puede ocurrir si, por ejemplo, una animación independiente está enlazada a la propiedad que se está leyendo.

La API es segura para subprocesos. Una aplicación puede llamar a cualquier método desde cualquier subproceso en cualquier momento. Sin embargo, dado que se debe llamar a muchos métodos de API en una secuencia determinada, sin ninguna sincronización, una aplicación puede experimentar un comportamiento imprevisible en función de cómo se intercalan los subprocesos. Por ejemplo, si dos subprocesos cambian la misma propiedad del mismo objeto a valores diferentes al mismo tiempo, la aplicación no puede predecir cuál de los dos valores será el valor final de la propiedad. Del mismo modo, si dos subprocesos llaman a [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) en el mismo dispositivo, ninguno de los subprocesos obtiene un comportamiento realmente transaccional porque una llamada a **Commit** en un subproceso envía el lote de todos los comandos emitidos por ambos subprocesos, no solo el que llamó a **Commit**.

El sistema mantiene todo el estado interno por objeto de dispositivo. Si una aplicación crea dos o más objetos de dispositivo DirectComposition, la aplicación puede mantener lotes independientes y otro estado entre los dos.

Todos los objetos DirectComposition tienen afinidad de objetos de dispositivo; Los objetos creados por un objeto de dispositivo determinado solo se pueden usar con ese objeto de dispositivo y solo se pueden asociar a otros objetos creados por el mismo objeto de dispositivo. En otras palabras, cada objeto de dispositivo es una isla independiente de funcionalidad. La única excepción es la clase visual , que permite la creación de árboles visuales donde un objeto visual puede pertenecer a un objeto de dispositivo diferente que su elemento primario. Esto permite escenarios en los que una aplicación y un control pueden administrar un único árbol de composición sin necesidad de compartir un único objeto de dispositivo DirectComposition.

## <a name="composition-engine"></a>Motor de composición

El motor de composición de DirectComposition se ejecuta en un proceso dedicado, independiente de cualquier proceso de aplicación. Un único proceso de composición, dwm.exe, admite todas las aplicaciones de una sesión. Cada aplicación puede crear dos árboles visuales para cada ventana que posee. Todos los árboles se implementan realmente como subárboles de un árbol visual mayor que también abarca las estructuras de composición de DWM. DwM crea un árbol visual grande para cada escritorio de una sesión. Estas son las principales ventajas de esta arquitectura:

-   El motor de composición tiene acceso a todos los mapas de bits de aplicación y árboles visuales, lo que permite la interoperabilidad y la composición de ventanas entre procesos.
-   El motor de composición se ejecuta en un proceso de sistema de confianza que es independiente de cualquier proceso de aplicación, lo que permite a las aplicaciones con derechos de acceso bajo crear contenido protegido de forma segura.
-   El motor de composición puede detectar cuándo una ventana determinada está totalmente ocluida y evitar perder los recursos de cpu y de unidad de procesamiento gráfico (GPU) que componen la ventana.
-   El motor de composición puede componer directamente en el búfer de reserva de pantalla, lo que evita la necesidad de una copia adicional necesaria para los motores de composición por proceso.
-   Todas las aplicaciones comparten un único dispositivo Direct3D para la composición, lo que ofrece un ahorro considerable de memoria.

El árbol visual es una estructura retenida. DirectComposition API expone métodos para editar la estructura en lotes de cambios que se procesan de forma atómica. El objeto raíz de DirectComposition API es el objeto de dispositivo, que actúa como generador para todos los demás objetos DirectComposition y contiene un método denominado [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit). El motor de composición no refleja los cambios que la aplicación realiza en el árbol  visual hasta que la aplicación llama a **Commit**, momento en el que todos los cambios desde la última confirmación se procesan como una transacción única.

El requisito de llamar a [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit) es similar al concepto de "fotograma", salvo que, dado que el motor de composición se ejecuta de forma asincrónica, puede presentar varios fotogramas diferentes entre las llamadas a **Commit**. En DirectComposition,  un fotograma es una iteración única del motor de composición y el intervalo empleado por una aplicación entre dos llamadas *a* **Commit** se denomina lote .

DirectComposition por lotes todas las llamadas de aplicación a DirectComposition API. La base de datos de objetos kernel, que se implementa en el controlador de sesión win32k.sys, almacena toda la información de estado asociada a las llamadas API.

El motor de composición genera un fotograma por cada espacio en blanco vertical de la pantalla. El marco se inicia en un espacio en blanco vertical y tiene como destino el espacio en blanco vertical subsiguiente. Cuando se inicia el fotograma, el motor de composición recoge todos los lotes pendientes e incluye sus comandos en ese marco. Los lotes se colocan en una cola pendiente cuando la aplicación llama a [**Commit**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-commit)y la cola pendiente se vacía de forma atómica al principio del marco. Por lo tanto, hay un único punto en el tiempo que marca el principio de un marco. Los lotes enviados antes de este punto se incluyen en el marco, mientras que los lotes enviados después de deben esperar hasta que se procese el fotograma siguiente. El bucle de composición completo es el siguiente:

1.  Calcule la hora del siguiente espacio en blanco vertical.
2.  Recupere todos los lotes pendientes.
3.  Procese los lotes recuperados.
4.  Actualice todas las animaciones con el tiempo estimado en el paso 1.
5.  Determine las regiones de la pantalla que se deben volver a componer.
6.  Vuelva a crear las regiones desusados.
7.  Para presentar el marco, voltear los búferes hacia atrás y los búferes frontales de cada pantalla.
8.  Si no se ha compuesto nada y se ha presentado en los pasos 6 y 7, espere a que se confirma un lote.
9.  Espere al siguiente espacio en blanco vertical.

Si hay varios monitores conectados a un único adaptador de vídeo, el motor de composición usa el espacio en blanco vertical del monitor principal para controlar el bucle de composición y establecer los tiempos de muestreo de animación. Cada monitor se representa mediante una cadena de volteo de pantalla completa independiente. el motor de composición repite los pasos 6 y 7 para cada monitor, de forma round robin, mediante un único dispositivo Direct3D. Si también hay varios adaptadores de vídeo, el motor de composición usa un dispositivo Direct3D independiente para cada adaptador de vídeo en los pasos 6 y 7.

Los fotogramas de composición están programados para iniciarse siempre en un espacio en blanco vertical, como se muestra en la ilustración siguiente.

![programación de fotogramas de composición](images/composition-frame-scheduling.png)

Si el motor de composición no tiene ningún trabajo que hacer porque el árbol de composición no ha cambiado, el subproceso de composición se suspensión mientras se espera un nuevo lote. Cuando se envía un nuevo lote, el subproceso de composición se reactiva, pero vuelve inmediatamente a suspensión hasta el siguiente espacio en blanco vertical. Este comportamiento garantiza tiempos de inicio y finalización de fotogramas predecibles para las aplicaciones y para el motor de composición.

El motor de composición publica los tiempos de presentación de fotogramas y la velocidad de fotogramas actual. La publicación de esta información permite a las aplicaciones calcular el tiempo de presentación de sus propios lotes, lo que a su vez permite sincronizar las animaciones. En concreto, una aplicación puede usar una combinación de estadísticas de fotogramas del motor de composición y un modelo histórico de cuánto tiempo tarda su subproceso de interfaz de usuario en generar un lote, para determinar el tiempo de muestreo de sus propias animaciones.

Por ejemplo, al principio del lote de la aplicación que se muestra en la ilustración anterior, la aplicación puede consultar el motor de composición para determinar el tiempo exacto de presentación del fotograma siguiente. A continuación, la aplicación puede usar la hora actual, junto con información sobre los lotes anteriores que ha generado, para determinar si la aplicación puede completar el lote actual antes del siguiente espacio en blanco vertical. Por lo tanto, la aplicación usa el tiempo de presentación del marco como tiempo de muestreo para sus propias animaciones. Si la aplicación determina que es poco probable que complete su trabajo en el espacio en blanco vertical actual, la aplicación puede usar el tiempo de fotograma posterior como tiempo de muestreo en su lugar, usando la información de velocidad de fotogramas devuelta por el motor de composición para calcular esa hora.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Conceptos de DirectComposition](directcomposition-concepts.md)
</dt> </dl>

 

 