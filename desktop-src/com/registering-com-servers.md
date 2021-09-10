---
title: Registro de servidores COM
description: Registro de servidores COM
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369443"
---
# <a name="registering-com-servers"></a>Registro de servidores COM

Después de haber definido una clase en el código (asegurándose de que implementa [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) o [**IClassFactory2)**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)y le ha asignado un CLSID, debe colocar información en el Registro que permita a COM, a petición de un cliente con el CLSID, crear instancias de sus objetos. Esta información indica al sistema, para un CLSID determinado, dónde se encuentra el código DLL o EXE de esa clase y cómo se va a iniciar.

Hay más de una manera de registrar una clase en el registro. Además, hay otras maneras de "registrar" una clase con el sistema cuando se ejecuta, de modo que el sistema sea consciente de que un objeto en ejecución está actualmente en el sistema.

Consulte los temas siguientes para obtener más información sobre el registro:

-   [Registro de una clase durante la instalación](registering-a-class-at-installation.md)
-   [Registro de un servidor EXE en ejecución](registering-a-running-exe-server.md)
-   [Registro de objetos en ROT](registering-objects-in-the-rot.md)
-   [Registro propio](self-registration.md)
-   [Instalación como aplicación de servicio](installing-as-a-service-application.md)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Responsabilidades del servidor COM](com-server-responsibilities.md)
</dt> </dl>

 

 