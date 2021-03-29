---
title: Claves del registro COM
description: Claves del registro COM
ms.assetid: 08406092-eb77-4001-a4fa-659ce945e4d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76b85bb84b0a6f2e6ccc233b68af2889f4cb11ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903524"
---
# <a name="com-registry-keys"></a>Claves del registro COM

El registro contiene una gran cantidad de información utilizada por COM. La información más importante se almacena en las claves siguientes.



| Clave                                                                 | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [AppID](appid-key.md)<br/>                                   | Agrupa las opciones de configuración (un conjunto de valores con nombre) para uno o varios objetos COM distribuidos en una ubicación del registro. Las subclaves bajo esta clave se usan para asignar un identificador de aplicación (AppID) a un nombre de servidor remoto. Para simplificar la administración de opciones de configuración y seguridad comunes, los objetos COM distribuidos hospedados por el mismo ejecutable se agrupan en un AppID.<br/>                                                                                                                                                                                                                                                                                                                      |
| [CLSID](clsid-key-hklm.md)<br/>                              | Un identificador de clase (CLSID) es un identificador único global que identifica un objeto de clase COM. Si el servidor o el contenedor permiten la vinculación a objetos incrustados, registre un CLSID para cada clase admitida de objetos. La clave CLSID contiene información utilizada por el controlador COM predeterminado para devolver información sobre una clase cuando está en estado de ejecución.<br/> Para obtener un CLSID para la aplicación, use uuidgen.exe, que se encuentra en el \\ directorio TOOLs del kit de herramientas de com, o use [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid). <br/>                                                                                                                                                                                       |
| [ProgID](-progid--key.md)<br/>                               | Un identificador de programación (ProgID) es una entrada del registro que se puede asociar a un CLSID. La clave ProgID asigna una cadena descriptiva para el usuario a un CLSID. Al igual que el CLSID, ProgID identifica una clase, pero con menos precisión. Use un ProgID en situaciones de programación en las que no sea posible usar un CLSID. Los ProgID no deben aparecer en la interfaz de usuario. No se garantiza que los ProgID sean únicos, por lo que solo se pueden usar cuando no se producen conflictos de nombres.<br/>                                                                                                                                                                                                                                                      |
| [VersionIndependentProgID](versionindependentprogid.md)<br/> | Asocia un ProgID a un CLSID. Se utiliza para determinar la versión más reciente de una aplicación de objeto. Al igual que el ProgID, el ProgID independiente de la versión se puede registrar con un nombre legible. <br/> Las aplicaciones deben registrar un identificador de programación independiente de la versión en la clave VersionIndependentProgID. El ProgID independiente de la versión hace referencia a la clase de la aplicación y no cambia de una versión a otra, sino a la constante restante en todas las versiones. Se usa con lenguajes de macros y hace referencia a la versión instalada actualmente de la clase de la aplicación. El ProgID independiente de la versión debe corresponder al nombre de la versión más reciente de la aplicación de objeto. <br/> |
| [extensión de archivo \_](-file-extension--key.md)<br/>              | Asocia una extensión de nombre de archivo a un ProgID.<br/> La información contenida en la clave de extensión de nombre de archivo la usan los [monikers](file-monikers.md)del sistema y del archivo. [**GetClassFile**](/windows/desktop/api/Objbase/nf-objbase-getclassfile) usa la clave de extensión de nombre de archivo para proporcionar el CLSID asociado. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                              |
| [Interfaz](interface-key.md)<br/>                           | Registra nuevas interfaces asociando un nombre de interfaz a un identificador de interfaz (IID). Asigna IID a información específica de una interfaz. La información es necesaria principalmente para el uso de interfaces a través de los límites del proceso. <br/> Al agregar una nueva interfaz, se debe completar la clave de interfaz para que COM registre la nueva interfaz. Debe haber una subclave IID para cada nueva interfaz. <br/>                                                                                                                                                                                                                                                                                                       |
| [OLE](hkey-local-machine-software-microsoft-ole.md)<br/>     | Controla los permisos de inicio y acceso predeterminados para los objetos COM distribuidos, así como las capacidades de seguridad de nivel de llamada para las aplicaciones que no llaman a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity). Solo los administradores tienen acceso total a esta parte del registro. El resto de usuarios tienen acceso de solo lectura. <br/>                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Registro de aplicaciones COM](registering-com-applications.md)
</dt> </dl>

 

 





