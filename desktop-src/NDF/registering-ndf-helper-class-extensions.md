---
title: Registro de extensiones de clase auxiliar NDF
description: Cada extensión de clase auxiliar tiene una serie de claves del registro asociadas. COM requiere algunas claves y NDF requiere algunas claves.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f211517a975bdef61db7937fffa95f13beddc156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103780208"
---
# <a name="registering-ndf-helper-class-extensions"></a>Registro de extensiones de clase auxiliar NDF

Cada extensión de clase auxiliar tiene una serie de claves del registro asociadas. COM requiere algunas claves y NDF requiere algunas claves.

## <a name="com-registry-keys"></a>Claves del registro COM

Las extensiones de clase auxiliares deben implementarse como servidores COM. Se debe completar el registro COM para cada extensión de clase auxiliar. Se debe registrar el CLSID del objeto, la interfaz [**INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) y la interfaz [**INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) . El registro crea un número de claves del registro relacionadas con COM para la extensión de clase auxiliar NDF.

## <a name="ndf-registry-keys"></a>Claves del registro NDF

Las extensiones de clase auxiliares deben registrarse antes de interactuar con el marco de diagnóstico de red y con otras clases auxiliares relacionadas. Esto se logra rellenando el registro.

En el procedimiento siguiente se muestra cómo agregar extensiones de clase auxiliar al registro.

1.  Publique los nombres de las clases auxiliares implementadas por el archivo DLL y sus dependencias mediante la creación de una clave para la DLL en

    **HKLM \\ System \\ CurrentControlSet \\ control \\ NetDiagFx** \\ *NombreProveedor* \\ **HostDLLs** \\ *clase de aplicación auxiliar* \\ **HelperClasses** \\ *nombre de clase auxiliar*

    Reemplace *NombreProveedor*, el *archivo dll de la clase auxiliar* y *el nombre de clase auxiliar* por valores definidos por el usuario, tal y como se describe a continuación.

    | Value               | Tipo    | Significado                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | *VendorName*        | Registro \_ SZ | Nombre del proveedor.                                                      |
    | *DLL de clase auxiliar*  | Registro \_ SZ | Nombre del archivo DLL, sin extensión.                                          |
    | *Nombre de clase auxiliar* | Registro \_ SZ | Nombre de la clase auxiliar de la que depende la clase auxiliar actual. |

    

     

2.  En cada clave de *nombre de clase auxiliar* , publique la siguiente información.

    

    | Value         | Tipo       | Significado                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **CLSID**     | Registro \_ SZ    | Cadena que contiene el identificador de clase COM de la clase auxiliar.                                                                                                            |
    | **Versión**   | Registro \_ SZ    | Una cadena que contiene las versiones principal y secundaria de la clase auxiliar en el formato <major> <minor> .                                                        |
    | **Publicado** | \_valor DWORD reg | Un valor de 1 significa que se espera que esta clase auxiliar se invoque directamente desde el cliente de diagnóstico. 0 significa que solo se puede llamar desde otra clase auxiliar. |
    | **Parent**    | Registro \_ SZ    | Cadena que nombra la clase auxiliar extensible de Microsoft que se va a extender.                                                                                       |

    

     

3.  Para cada clase auxiliar, publique la lista de atributos coincidentes mediante la creación de una clave en

    **HKLM \\ System \\ CurrentControlSet \\ control \\ NetDiagFx** \\ *NombreProveedor* \\ **HostDLLs** \\ *clase auxiliar* \\ **HelperClasses** \\ *nombre de clase auxiliar* \\ **MatchAttributes**

    La clave debe contener uno o más valores (uno por atributo) del tipo siguiente.

    | Value             | Tipo                             | Significado                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | **AttributeName** | REG. reg. \_ \| \_ DWORD \| reg \_ binario | Valor que completa el par de nombre y valor para un atributo determinado. |

    

     

 

 




