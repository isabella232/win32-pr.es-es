---
title: Claves del Registro COM
description: Claves del Registro COM
ms.assetid: 08406092-eb77-4001-a4fa-659ce945e4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b85bb84b0a6f2e6ccc233b68af2889f4cb11ab
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369564"
---
# <a name="com-registry-keys"></a>Claves del Registro COM

El registro contiene una gran cantidad de información utilizada por COM. La información más importante se almacena en las claves siguientes.



| Clave                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AppID](appid-key.md)<br/>                                   | Agrupa las opciones de configuración (un conjunto de valores con nombre) para uno o varios objetos COM distribuidos en una ubicación del Registro. Las subclaves de esta clave se usan para asignar un identificador de aplicación (AppID) a un nombre de servidor remoto. Para simplificar la administración de valores de configuración y seguridad comunes, los objetos COM distribuidos hospedados por el mismo ejecutable se agrupan en un AppID.<br/>                                                                                                                                                                                                                                                                                                                      |
| [CLSID](clsid-key-hklm.md)<br/>                              | Un identificador de clase (CLSID) es un identificador único global que identifica un objeto de clase COM. Si el servidor o contenedor permite la vinculación a objetos incrustados, registre un CLSID para cada clase de objetos admitida. La clave CLSID contiene información utilizada por el controlador COM predeterminado para devolver información sobre una clase cuando está en estado de ejecución.<br/> Para obtener un CLSID para la aplicación, use uuidgen.exe, que se encuentra en el directorio TOOLs del Toolkit COM, o \\ [**use CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid). <br/>                                                                                                                                                                                       |
| [ProgID](-progid--key.md)<br/>                               | Un identificador de programación (ProgID) es una entrada del Registro que se puede asociar a un CLSID. La clave ProgID asigna una cadena fácil de usar a un CLSID. Al igual que el CLSID, progID identifica una clase, pero con menos precisión. Use un ProgID en situaciones de programación en las que no es posible usar un CLSID. Los progID no deben aparecer en la interfaz de usuario. No se garantiza que los progID sean únicos, por lo que solo se pueden usar cuando no se producen conflictos de nombres.<br/>                                                                                                                                                                                                                                                      |
| [VersionIndependentProgID](versionindependentprogid.md)<br/> | Asocia un ProgID a un CLSID. Se usa para determinar la versión más reciente de una aplicación de objeto. Al igual que progID, el ProgID independiente de la versión se puede registrar con un nombre legible para el usuario. <br/> Las aplicaciones deben registrar un identificador de programación independiente de la versión en la clave VersionIndependentProgID. ProgID independiente de la versión hace referencia a la clase de la aplicación y no cambia de versión a versión, sino que permanece constante en todas las versiones. Se usa con lenguajes de macro y hace referencia a la versión instalada actualmente de la clase de la aplicación. El ProgID independiente de la versión debe corresponder al nombre de la versión más reciente de la aplicación de objeto. <br/> |
| [extensión de \_ archivo](-file-extension--key.md)<br/>              | Asocia una extensión de nombre de archivo a un ProgID.<br/> Tanto el sistema como los [monikers](file-monikers.md)de archivos usan la información contenida en la clave de extensión de nombre de archivo. [**GetClassFile usa**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) la clave de extensión de nombre de archivo para proporcionar el CLSID asociado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Interfaz](interface-key.md)<br/>                           | Registra nuevas interfaces asociando un nombre de interfaz con un identificador de interfaz (IID). Asigna LOS IID a información específica de una interfaz. La información es necesaria principalmente para usar interfaces a través de los límites del proceso. <br/> Al agregar una nueva interfaz, la clave de interfaz debe completarse para que COM registre la nueva interfaz. Debe haber una subclave IID para cada nueva interfaz. <br/>                                                                                                                                                                                                                                                                                                       |
| [Ole](hkey-local-machine-software-microsoft-ole.md)<br/>     | Controla los permisos de inicio y acceso predeterminados para los objetos COM distribuidos, así como las funcionalidades de seguridad de nivel de llamada para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Solo los administradores tienen acceso total a esta parte del registro. Todos los demás usuarios tienen acceso de solo lectura. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 





