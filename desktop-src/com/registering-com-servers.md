---
title: Registrar servidores COM
description: Registrar servidores COM
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104149642"
---
# <a name="registering-com-servers"></a>Registrar servidores COM

Después de haber definido una clase en el código (asegurándose de que implementa [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) o [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) y le ha asignado un CLSID, debe colocar información en el registro que permita que com, a petición de un cliente con el CLSID, cree instancias de sus objetos. Esta información indica al sistema, para un CLSID determinado, donde se encuentra el código del archivo DLL o EXE para esa clase y cómo se inicia.

Hay más de una manera de registrar una clase en el registro. Además, hay otras maneras de "registrar" una clase en el sistema cuando se está ejecutando, de modo que el sistema tenga en cuenta que un objeto en ejecución está actualmente en el sistema.

Vea los temas siguientes para obtener más información acerca del registro:

-   [Registrar una clase durante la instalación](registering-a-class-at-installation.md)
-   [Registrar un servidor EXE en ejecución](registering-a-running-exe-server.md)
-   [Registrar objetos en la tabla ROT](registering-objects-in-the-rot.md)
-   [Registro automático](self-registration.md)
-   [Instalar como una aplicación de servicio](installing-as-a-service-application.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Responsabilidades del servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 