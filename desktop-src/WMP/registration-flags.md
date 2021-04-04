---
title: Marcas de registro
description: Marcas de registro
ms.assetid: ba1709c2-0fe5-4168-9aed-613d01eff21f
keywords:
- Complementos de Media Player de Windows, marcas de registro
- complementos, marcas de registro
- Complementos de la interfaz de usuario, marcas de registro
- Complementos de la interfaz de usuario, marcas de registro
- marcas, Complementos de la interfaz de usuario
- registro, Complementos de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac609b45866cd5f18edf61dffc2d3b7ac3c397ac
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/19/2020
ms.locfileid: "104077327"
---
# <a name="registration-flags"></a>Marcas de registro

Cuando el Asistente para complementos de Windows Media Player crea un nuevo proyecto de complemento de interfaz de usuario, crea una clave en el registro que contiene información sobre el complemento. Esta clave se crea en la siguiente ubicación:


```C++
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\MediaPlayer\UIPlugins\{ClassId}
```



*ClassID* es el ID. de clase del complemento.

Esta clave incluye los valores siguientes.



| Nombre                     | Tipo       | Descripción                                                                                                                                                                               |
|--------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Funcionalidades             | \_valor DWORD reg | Un valor DWORD que consta de al menos una marca de tipo de complemento que se puede combinar con una o más marcas de funciones de complemento mediante operaciones binarias o.                             |
| Descripción              | Registro \_ SZ    | Cadena que contiene la descripción del complemento. El Asistente para complementos crea un recurso de cadena y proporciona la dirección URL del recurso (mediante el protocolo res) para este valor.         |
| FriendlyName             | Registro \_ SZ    | Cadena que contiene el nombre legible por el usuario para el complemento. El Asistente para complementos crea un recurso de cadena y proporciona la dirección URL del recurso (mediante el protocolo res) para este valor. |
| UninstallPath (opcional) | Registro \_ SZ    | Cadena que contiene la ruta de acceso a un archivo ejecutable que desinstala el complemento.                                                                                                        |



 

Para obtener más información sobre el protocolo res, vea el SDK de desarrollo de Internet.

En la tabla siguiente se detallan las marcas de tipo de complemento.



| Marca de tipo de complemento                | Value | Descripción                                       |
|----------------------------------|-------|---------------------------------------------------|
| **\_fondo de tipo de complemento \_**     | 0x1   | El complemento de la interfaz de usuario no muestra una interfaz de usuario. |
| **tipo de complemento \_ \_ SEPARATEWINDOW** | 0x2   | El complemento de la interfaz de usuario es un complemento de ventana independiente.      |
| **tipo de complemento \_ \_ DISPLAYAREA**    | 0x3   | El complemento de la interfaz de usuario es un complemento de área de presentación.         |
| **tipo de complemento \_ \_ SETTINGSAREA**   | 0x4   | El complemento de la interfaz de usuario es un complemento de área de configuración.        |
| **tipo de complemento \_ \_ METADATAAREA**   | 0X5   | El complemento de la interfaz de usuario es un complemento de área de metadatos.        |



 

En la tabla siguiente se detallan las marcas de funcionalidades del complemento.



| Marca de capacidades del complemento             | Value      | Descripción                                                                                                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **marcas de COMPLEMENTOs \_ \_ ACCEPTSMEDIA**       | 0x10000000 | El complemento de interfaz de usuario puede aceptar matrices de punteros de objetos **multimedia** cuando Windows Media Player llama a [**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                           |
| **marcas de COMPLEMENTOs \_ \_ ACCEPTSPLAYLISTS**   | 0x8000000  | El complemento de interfaz de usuario puede aceptar matrices de punteros de objeto de **lista de reproducción** cuando Windows Media Player llama a [**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty) .                                                                                                                                                                                                                                                        |
| **marcas de COMPLEMENTOs \_ \_ HASPRESETS**         | 0x4000000  | El complemento de la interfaz de usuario usa valores preestablecidos. Si el complemento especifica esta marca, Windows Media Player consultará el complemento para obtener información preestablecida mediante una llamada a [**IWMPPluginUI:: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty) .                                                                                                                                                                                                      |
| **marcas de COMPLEMENTOs \_ \_ HASPROPERTYPAGE**    | 0x80000000 | El complemento de la interfaz de usuario proporciona un cuadro de diálogo de página de propiedades. Windows Media Player llamará a [**IWMPPluginUI::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) si esta marca se establece cuando se invoca la página de propiedades.                                                                                                                                                                                                 |
| **marcas de complemento \_ \_ ocultas**             | 0x02000000 | El complemento de la interfaz de usuario de fondo no aparece en el menú **Complementos** al que se tiene acceso desde los menús **Ver** o **herramientas** o el botón **seleccionar ahora opciones de reproducción** en reproducción en curso. Aparece en la pestaña complementos del **cuadro de diálogo** opciones. Esto hace que el icono de ejecución del complemento de fondo aparezca en la barra de estado. Esta marca no tiene ningún efecto en los complementos que no sean los complementos de la interfaz de usuario de fondo.<br/> |
| **marcas de COMPLEMENTOs \_ \_ INSTALLAUTORUN**     | 0x40000000 | Windows Media Player ejecuta el complemento de la interfaz de usuario automáticamente cuando se instala el complemento.                                                                                                                                                                                                                                                                                                                               |
| **marcas de COMPLEMENTOs \_ \_ LAUNCHPROPERTYPAGE** | 0x20000000 | Windows Media Player llama a [**IWMPPluginUI::D isplaypropertypage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage) cuando el complemento de la interfaz de usuario se ejecuta por primera vez. Si se especifica esta marca, también se deben especificar las **marcas de complemento \_ \_ HASPROPERTYPAGE** .<br/>                                                                                                                                                             |



 

Las siguientes constantes se definen en wmpplug. h. No cambie los valores asociados a estas constantes.



| Nombre                                    | Descripción                               |
|-----------------------------------------|-------------------------------------------|
| **COMPLEMENTO \_ INSTALLREGKEY**               | Ubicación de la clave del registro del complemento. |
| **COMPLEMENTO \_ INSTALLREGKEY \_ FRIENDLYNAME** | Nombre del valor de nombre descriptivo.      |
| **\_Descripción de INSTALLREGKEY de complemento \_**  | Nombre del valor de descripción.        |
| **\_funcionalidades de INSTALLREGKEY de complementos \_** | Nombre del valor de capacidades.       |
| **desinstalación de INSTALLREGKEY de COMPLEMENTOs \_ \_**    | Nombre del valor de la ruta de desinstalación.     |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**IWMPPluginUI::D isplayPropertyPage**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-displaypropertypage)
</dt> <dt>

[**IWMPPluginUI:: GetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-getproperty)
</dt> <dt>

[**IWMPPluginUI:: SetProperty**](/previous-versions/windows/desktop/api/wmpplug/nf-wmpplug-iwmppluginui-setproperty)
</dt> <dt>

[**Referencia de programación de complementos de interfaz de usuario**](user-interface-plug-ins-programming-reference.md)
</dt> </dl>

 

 





