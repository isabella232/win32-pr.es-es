---
title: Windows Arquitectura de Administrador de dispositivos multimedia
description: Windows Arquitectura de Administrador de dispositivos multimedia
ms.assetid: 3c1b2da4-559d-427b-b502-5ef8dc055a8e
keywords:
- Windows Arquitectura Administrador de dispositivos multimedia
- Administrador de dispositivos,architecture
- arquitectura de Windows Media Administrador de dispositivos
- Windows Aplicaciones Administrador de dispositivos multimedia, aplicaciones de escritorio
- Administrador de dispositivos,aplicaciones de escritorio
- Windows Media Administrador de dispositivos, proveedores de servicios
- Administrador de dispositivos,proveedores de servicios
- Windows Archivos Administrador de dispositivos, complementos
- Administrador de dispositivos,complementos
- aplicaciones de escritorio, Windows de Administrador de dispositivos multimedia
- proveedores de servicios, Windows arquitectura de Administrador de dispositivos multimedia
- complementos, arquitectura Windows de Administrador de dispositivos multimedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9fda87e4ed4bce2c82bbb9c0863c119851965940
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127242576"
---
# <a name="windows-media-device-manager-architecture"></a>Windows Arquitectura de Administrador de dispositivos multimedia

Windows El Administrador de dispositivos permite que una aplicación o complemento se comunique con un dispositivo. Las aplicaciones pueden solicitar metadatos de dispositivo, enumerar y explorar los dispositivos conectados y enviar o recibir objetos (carpetas, archivos, listas de reproducción, entre otros). Windows Media Administrador de dispositivos proporciona una única API a la aplicación que realiza la llamada, independientemente del tipo de dispositivo al que se llame (clase MTP o Storage masiva, proveedores de servicios basados en la versión 10 o proveedores de servicios basados en versiones anteriores de Windows Media Administrador de dispositivos).

Windows El Administrador de dispositivos multimedia actúa como un equilibrio entre los tres componentes principales del sistema: la aplicación, que realiza solicitudes (para obtener información, para leer o escribir datos, y así sucesivamente); un proveedor de contenido seguro, que es un componente que controla la comunicación con archivos protegidos por DRM; y un proveedor de servicios, que recibe solicitudes de la aplicación y se comunica con el dispositivo para realizar estas solicitudes. Tanto la aplicación como el proveedor de servicios se basa en Windows Media Administrador de dispositivos SDK.

En el diagrama siguiente se muestra cómo una aplicación de escritorio se comunica con un dispositivo mediante Windows Media Administrador de dispositivos 11.

![diagrama que muestra una aplicación que se comunica con cuatro tipos diferentes de dispositivos.](images/wmdm-device-communication.gif)

En el diagrama anterior se muestra una aplicación que se comunica con cuatro tipos diferentes de dispositivos, cada uno con su propio proveedor de servicios. Cada proveedor de servicios está diseñado para comunicarse con un tipo específico de dispositivo. En este diagrama se muestran los tres proveedores de servicios proporcionados por Microsoft (controladores de clase genéricos para dispositivos mass Storage Class, dispositivos RAPI y dispositivos MTP), así como un proveedor de servicios personalizado para un dispositivo propietario creado por un tercero. Cuando se conecta un dispositivo, Windows media Administrador de dispositivos crea una instancia del proveedor de servicios registrado para ese dispositivo. Los proveedores de servicios obtienen solicitudes de la aplicación a través de interfaces de Windows Media Administrador de dispositivos que implementan, usan los controladores adecuados para comunicarse con el dispositivo y devuelven los resultados adecuados. La comunicación entre el proveedor de servicios y el dispositivo está fuera del dominio de Windows Media Administrador de dispositivos.

Los proveedores de servicios son invisibles para la aplicación; Una aplicación solo ve una lista de "dispositivos" porque Windows Media Administrador de dispositivos expone un conjunto estándar de métodos e interfaces para todos los dispositivos. Si un fabricante crea un proveedor de servicios personalizado, debe controlar todos los métodos Windows Media Administrador de dispositivos estándar si las aplicaciones pueden usar el dispositivo.

En este diagrama también se muestra un módulo de proveedor de contenido seguro (SCP). Este módulo es responsable de controlar el contenido protegido de Administración de derechos digitales (DRM). Microsoft proporciona un módulo SCP que puede controlar archivos WMA y WMV protegidos con DRM. Si una aplicación o dispositivo pretende controlar otros formatos protegidos, debe proporcionar su propio módulo SCP. Ni la aplicación ni el proveedor de servicios se ocupa directamente del SCP.

Tanto la aplicación como el proveedor de servicios se basa en Windows Media Administrador de dispositivos, que enruta las llamadas entre la aplicación y el proveedor de servicios adecuado para un dispositivo. el proveedor de servicios es responsable de comunicarse directamente con el dispositivo. Windows Los Administrador de dispositivos realizan algunas acciones (por ejemplo, enumerar dispositivos conectados, enrutar llamadas y controlar la comprobación de componentes); sin embargo, la mayor parte del trabajo lo realiza el proveedor de servicios, que recibe solicitudes de la aplicación y se comunica con el dispositivo.

Una aplicación creada en Windows Media Administrador de dispositivos puede comunicarse con dispositivos y proveedores de servicios basados en versiones anteriores de Windows Media Administrador de dispositivos; Sin embargo, estos dispositivos anteriores se ejecutarán a través de componentes de la serie 9 (no se muestran) y no admitirán las características más recientes, especialmente la tecnología de administración de derechos digitales más avanzada.

Arquitectura de un dispositivo

En el diagrama siguiente se muestra una jerarquía simplificada de dispositivos y almacenamientos, tal como lo ve una aplicación que usa Windows Media Administrador de dispositivos.

![diagrama que muestra los almacenamientos en un dispositivo.](images/wmdm-basic-device-layout.gif)

En el diagrama anterior se muestra una versión simplificada de una unidad flash conectada, como se ve en una Windows de Administrador de dispositivos multimedia. La unidad flash tiene atributos y propiedades, como un número de serie y configuraciones de formato admitidas. Un elemento secundario inmediato del dispositivo flash es el objeto de almacenamiento raíz, que contiene una carpeta, que a su vez contiene una imagen y una canción.

Una aplicación enumera la lista de dispositivos conectados mediante una llamada a un método de enumeración expuesto por la interfaz [**IWMDeviceManager**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdevicemanager) raíz. Los dispositivos se representan mediante [**una interfaz IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) (o una interfaz derivada). Esta interfaz expone métodos para recuperar el nombre del dispositivo, las funcionalidades de formato, el número de serie, entre otros, así como un método que enumera los *almacenamientos* en el dispositivo. En Windows de Administrador de dispositivos, un almacenamiento es cualquier tipo de objeto en el dispositivo, independientemente de si se trata o no de un blob de datos real. Por ejemplo: los archivos de audio, los archivos de texto, las carpetas, las listas de reproducción almacenadas como archivos y las listas de reproducción almacenadas como metadatos se consideran almacenamientos, aunque es probable que las carpetas y los elementos de metadatos no representen un archivo físico. El tipo (o formato) de un almacenamiento se puede recuperar llamando a [**GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) (o [**GetMetadata,**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)solicitando el formato del almacenamiento).

Los almacenamientos de un dispositivo se almacenan jerárquicamente y todos los dispositivos tienen un almacenamiento raíz. Cada almacenamiento puede contener cero o más objetos secundarios, enumerados llamando al método [**IWMDMStorage::EnumStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-enumstorage) de ese almacenamiento.

Tenga en cuenta que cada almacenamiento del diagrama tiene atributos y metadatos asociados (no se muestran todos los valores). Los atributos son información booleana simple que a menudo describe información de administración o navegación (como "tiene carpetas" o "puede eliminar"), mientras que los metadatos pueden ser valores de cadena, números o información compleja (como las funcionalidades de representación). Los atributos se describen mediante un conjunto bastante limitado de marcas definidas por el SDK y recuperadas mediante una llamada a [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) o [**IWMDMStorage2::GetAttributes2.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage2-getattributes2) Los valores de metadatos se recuperan mediante un nombre único; el SDK define una serie de valores de metadatos que los dispositivos deben admitir, pero los dispositivos pueden definir sus [propias constantes de metadatos.](metadata-constants.md) Sin embargo, si un proveedor de servicios o dispositivos define una nueva constante de metadatos, las aplicaciones no podrán solicitar ni establecer este valor a menos que los desarrolladores de aplicaciones conozcan esta nueva constante. Un proveedor de servicios debe admitir [**IWMDMStorage3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage3) o posterior para poder recuperar o establecer metadatos. Para obtener más información, vea [Obtener y establecer metadatos y atributos.](getting-and-setting-metadata-and-attributes.md)

Proveedores de servicios

El proveedor de servicios actúa como intermediario entre la aplicación y el dispositivo. El proveedor de servicios es invisible para el desarrollador de aplicaciones, por lo que un desarrollador de aplicaciones no necesita saber nada sobre el desarrollo de un proveedor de servicios. Sin embargo, es el proveedor de servicios el que realiza el trabajo de comunicación con un dispositivo.

Un proveedor de servicios es un archivo DLL COM basado en Windows Media Administrador de dispositivos que recibe solicitudes de una aplicación y se comunica con el dispositivo para realizarlas. La comunicación con la aplicación de escritorio se media mediante Windows Media Administrador de dispositivos; la comunicación con el dispositivo está bajo el control del proveedor de servicios.

Un proveedor de servicios recibe solicitudes de la aplicación para enumerar el contenido del dispositivo, solicitudes de funcionalidades del dispositivo, solicitudes para leer o escribir datos, y así sucesivamente. Debe conocer el diseño de un dispositivo lo suficientemente bien como para poder enviar comandos con el formato y el protocolo adecuados. También debe poder ocultar los requisitos específicos del dispositivo, como una extensión de archivo necesaria para las listas de reproducción, para que las aplicaciones no necesiten conocer estos requisitos para poder usar el dispositivo.

Microsoft proporciona una serie de proveedores de servicios para los tipos de dispositivos estándar, incluidos los dispositivos MTP genéricos, los dispositivos de Storage class masivos y los dispositivos RAPI. La única razón por la que un diseñador de dispositivos debe tener que crear un proveedor de servicios personalizado es si un dispositivo tiene algunos requisitos de almacenamiento de datos específicos o inusuales que los proveedores de servicios estándar no controlan, por ejemplo, si los archivos deben almacenarse en ubicaciones específicas y el sistema operativo del dispositivo no lo controla automáticamente.

Cuando un dispositivo está conectado al equipo, el sistema operativo crea una instancia del proveedor de servicios adecuado para cada aplicación Windows Media Administrador de dispositivos aplicación. Si se inicia Windows aplicación Administrador de dispositivos media, se cargará una segunda instancia del proveedor de servicios. Sin embargo, cada proveedor de servicios puede controlar varios dispositivos. En el diagrama siguiente se ilustra esto.

![diagrama que muestra dos dispositivos mtp que se comunican con dos aplicaciones.](images/wmdm-sp-to-device.gif)

En el diagrama anterior se muestran dos aplicaciones diferentes que se comunican con dos dispositivos MTP. Los dispositivos usan la misma clase de proveedor de servicios, pero cada aplicación tiene su propia instancia del mismo proveedor de servicios. Cada instancia del proveedor de servicios se comunica con los dispositivos. Las distintas instancias del proveedor de servicios no se conocen entre sí.

Muchos métodos de aplicación tienen un método de proveedor de servicios con nombre correspondiente. Cuando la aplicación llama a un método, Windows Media Administrador de dispositivos enruta la llamada al método correspondiente en el proveedor de servicios (aunque podría realizar algunas acciones internas adicionales primero). Por ejemplo, cuando la aplicación llama a [**IWMDMDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty), Windows Media Administrador de dispositivos enruta esta llamada a la implementación del proveedor de servicios de [**IMDSPDevice3::GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice3-getproperty). (La mayoría de las interfaces de aplicación comienzan por IWMDM y la interfaz del proveedor de servicios correspondiente comienza con IMDSP). Se espera que el proveedor de servicios controle esta llamada al método y devuelva un resultado adecuado.

Una aplicación nunca explora ni se comunica con un dispositivo directamente (a menos que llame a [**IWMDMDevice3::D eviceIoControl**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) o [**IWMDMStorage::SendOpaqueCommand**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-sendopaquecommand)); la aplicación se comunica con el proveedor de servicios, que debe representar un dispositivo de la manera más lógica y sencilla posible. Cuando la aplicación solicita información sobre el dispositivo o enumera objetos en el dispositivo, el proveedor de servicios consulta el dispositivo de la manera adecuada y adquiere y devuelve la información adecuada. Puede exponer la organización de archivos en el dispositivo de forma diferente de cómo se almacena físicamente en el dispositivo, si es adecuado. Sin embargo, expone el dispositivo, debe ser coherente y lógico para permitir que la aplicación encuentre lo que necesita y controle los comandos que envía. Un buen proveedor de servicios ocultará las localidades específicas del dispositivo; por ejemplo, si el dispositivo almacena físicamente una lista de reproducción como un archivo con una extensión de archivo personalizada, el proveedor de servicios debe agregar esa extensión automáticamente cuando la aplicación crea una lista de reproducción en el dispositivo. no debe esperar que la aplicación conozca la extensión adecuada al crear un objeto de lista de reproducción.

Los proveedores de servicios se ejecutan dentro del proceso de la aplicación que realiza la llamada. La única excepción a esto es el proveedor de servicios MTP, que se ejecuta en su propio proceso. Por este motivo, existe el riesgo de que un proveedor de servicios bloqueado haga que la aplicación que realiza la llamada se bloquee. Por lo tanto, los proveedores de servicios deben diseñarse para ser sólidos y evitar el bloqueo, y las aplicaciones deben diseñarse para evitar la detención si una llamada de método determinado no se devuelve rápidamente.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Tareas iniciales**](getting-started.md)
</dt> </dl>

 

 




