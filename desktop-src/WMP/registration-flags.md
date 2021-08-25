---
title: Marcas de registro
description: Marcas de registro
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Reproductor de Windows Media complementos, marcas de registro
- complementos, marcas de registro
- complementos de interfaz de usuario, marcas de registro
- Complementos de interfaz de usuario, marcas de registro
- flags,user interface plug-ins
- registro, complementos de interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afbd34ed98236f8a02c936d52b092b82be60b986fb7b16edce1f3b1cbb91d6a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002815"
---
# <a name="registration-flags"></a>Marcas de registro

Cuando el Reproductor de Windows Media complemento crea un nuevo proyecto de complemento de interfaz de usuario, crea una clave en el Registro que contiene información sobre el complemento. Esta clave se crea en la siguiente ubicación:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



*ClassId* es el identificador de clase del complemento.

Esta clave incluye los siguientes valores.



| Nombre                     | Tipo       | Descripción                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funcionalidades             | REG \_ DWORD | Valor DWORD que consta de al menos una marca de tipo de complemento que se puede combinar con una o varias marcas de funcionalidades de complemento mediante operaciones OR binarias.                             |
| Descripción              | REG \_ SZ    | Cadena que contiene la descripción del complemento. El asistente para complementos crea un recurso de cadena y proporciona la dirección URL del recurso (mediante el protocolo res) para este valor.         |
| FriendlyName             | REG \_ SZ    | Cadena que contiene el nombre legible por el usuario para el complemento. El asistente para complementos crea un recurso de cadena y proporciona la dirección URL del recurso (mediante el protocolo res) para este valor. |
| UninstallPath (opcional) | REG \_ SZ    | Cadena que contiene la ruta de acceso a un archivo ejecutable que desinstala el complemento.                                                                                                        |



 

Para obtener más información sobre el protocolo res, consulte el SDK de desarrollo de Internet.

En la tabla siguiente se detallan las marcas de tipo de complemento.



| Marca de tipo de complemento                | Value | Descripción                                       |
|----------------------------------|-------|---------------------------------------------------|
| **FONDO \_ DEL TIPO DE \_ COMPLEMENTO**     | 0x1   | El complemento de interfaz de usuario no muestra una interfaz de usuario. |
| **TIPO \_ DE COMPLEMENTO \_ SEPARATEWINDOW** | 0x2   | El complemento de interfaz de usuario es un complemento de ventana independiente.      |
| **TIPO \_ DE \_ COMPLEMENTO DISPLAYAREA**    | 0x3   | El complemento de interfaz de usuario es un complemento de área de presentación.         |
| **CONFIGURACIÓN \_ DEL TIPO DE \_ COMPLEMENTOAREA**   | 0x4   | El complemento de interfaz de usuario es un complemento de área de configuración.        |
| **METADATOS \_ DEL TIPO DE \_ COMPLEMENTOAREA**   | 0x5   | El complemento de interfaz de usuario es un complemento de área de metadatos.        |



 

En la tabla siguiente se detallan las marcas de funcionalidades del complemento.



| Marca de funcionalidades de complemento             | Value      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **MARCAS \_ DE COMPLEMENTO \_ ACCEPTSMEDIA**       | 0x10000000 | El complemento de interfaz de usuario puede **aceptar** matrices de punteros de objeto Multimedia Reproductor de Windows Media llama a [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                           |
| **MARCAS \_ DE COMPLEMENTO \_ ACCEPTSPLAYLISTS**   | 0x8000000  | El complemento de interfaz de usuario puede aceptar matrices de punteros de objeto **de** lista de reproducción Reproductor de Windows Media llama a [**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                        |
| **MARCAS \_ DE COMPLEMENTO \_ HASPRESETS**         | 0x4000000  | El complemento de interfaz de usuario usa valores preestablecidos. Si el complemento especifica esta marca, Reproductor de Windows Media consultará el complemento para obtener información preestablecida llamando a [**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .                                                                                                                                                                                                      |
| **MARCAS \_ DE COMPLEMENTO \_ HASPROPERTYPAGE**    | 0x80000000 | El complemento de interfaz de usuario proporciona un cuadro de diálogo de página de propiedades. Reproductor de Windows Media llamará a [**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) si esta marca se establece cuando se invoca la página de propiedades.                                                                                                                                                                                                 |
| **MARCAS \_ DE COMPLEMENTO \_ OCULTAS**             | 0x02000000 | El complemento de interfaz de usuario en segundo plano no aparece  en  el menú Complementos  al que se tiene acceso desde los menús Ver o Herramientas o el botón Seleccionar opciones De reproducción ahora en Reproducción ahora.  Aparece en la pestaña **Complementos del** cuadro de diálogo Opciones. Hace que el icono Background Plug-in Running (Ejecución del complemento en segundo plano) aparezca en la barra de estado. Esta marca no tiene ningún efecto en los complementos que no son complementos de interfaz de usuario en segundo plano.<br/> |
| **MARCAS \_ DE COMPLEMENTO \_ INSTALLAUTORUN**     | 0x40000000 | Reproductor de Windows Media el complemento de interfaz de usuario se ejecuta automáticamente cuando se instala el complemento.                                                                                                                                                                                                                                                                                                                               |
| **MARCAS \_ DE COMPLEMENTO \_ LAUNCHPROPERTYPAGE** | 0x20000000 | Reproductor de Windows Media llama a [**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) cuando el complemento de interfaz de usuario se ejecuta por primera vez. Si se especifica esta marca, también se debe especificar **\_ PLUGIN FLAGS \_ HASPROPERTYPAGE.**<br/>                                                                                                                                                             |



 

Las siguientes constantes se definen en wmpplug.h. No cambie los valores asociados a estas constantes.



| Nombre                                    | Descripción                               |
|-----------------------------------------|-------------------------------------------|
| **PLUGIN \_ INSTALLREGKEY**               | Ubicación de la clave del Registro del complemento. |
| **PLUGIN \_ INSTALLREGKEY \_ FRIENDLYNAME** | Nombre del valor de nombre descriptivo.      |
| **DESCRIPCIÓN \_ DE INSTALLREGKEY DEL \_ COMPLEMENTO**  | Nombre del valor de descripción.        |
| **FUNCIONALIDADES \_ INSTALLREGKEY DEL \_ COMPLEMENTO** | Nombre del valor de las funcionalidades.       |
| **COMPLEMENTO \_ INSTALLREGKEY \_ UNINSTALL**    | Nombre del valor de la ruta de acceso de desinstalación.     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[**IWMPPluginUI::GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[**IWMPPluginUI::SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[**Interfaz de usuario de programación de complementos**](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





