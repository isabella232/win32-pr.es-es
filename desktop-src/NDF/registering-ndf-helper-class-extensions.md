---
title: Registro de extensiones de clase auxiliar de NDF
description: Cada extensión de clase auxiliar tiene varias claves del Registro asociadas. Algunas claves son necesarias para COM y otras son necesarias para NDF.
ms.assetid: 9ff3266d-5ffc-4a00-be24-2f85461c6ea6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 166f07760dc8905f35c82c63d58fa2faa804aeb8
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122883831"
---
# <a name="registering-ndf-helper-class-extensions"></a>Registro de extensiones de clase auxiliar de NDF

Cada extensión de clase auxiliar tiene varias claves del Registro asociadas. Algunas claves son necesarias para COM y otras son necesarias para NDF.

## <a name="com-registry-keys"></a>Claves del Registro COM

Las extensiones de clase auxiliar deben implementarse como servidores COM. El registro COM debe completarse para cada extensión de clase auxiliar. El CLSID del objeto, la [**interfaz INetDiagHelperInfo**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelperinfo) y la [**interfaz INetDiagHelper**](/windows/desktop/api/ndhelper/nn-ndhelper-inetdiaghelper) deben estar registrados. El registro crea una serie de claves del Registro relacionadas con COM para la extensión de clase auxiliar de NDF.

## <a name="ndf-registry-keys"></a>Claves del Registro de NDF

Las extensiones de clase auxiliar deben registrarse antes de interactuar con el Marco de diagnóstico de redes y con otras clases auxiliares relacionadas. Para ello, se rellenará el registro.

En el procedimiento siguiente se muestra cómo agregar extensiones de clase auxiliar al Registro.

1.  Publique los nombres de las clases auxiliares implementadas por el archivo DLL y sus dependencias mediante la creación de una clave para el archivo DLL en

    **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper Class* \\ **HelperClasses** \\ *Helper Class Name*

    Reemplace *VendorName*, *DLL de clase auxiliar* y Nombre *de* clase auxiliar por valores definidos por el usuario, como se describe a continuación.

    | Valor               | Tipo    | Significado                                                                      |
    |---------------------|---------|------------------------------------------------------------------------------|
    | *VendorName*        | REG \_ SZ | Nombre del proveedor.                                                      |
    | *DLL de clase auxiliar*  | REG \_ SZ | Nombre del archivo DLL, sin extensión.                                          |
    | *Nombre de clase del asistente* | REG \_ SZ | Nombre de la clase auxiliar de la que depende la clase auxiliar actual. |

    

     

2.  En cada clave *del nombre de clase* auxiliar, publique la siguiente información.

    

    | Valor         | Tipo       | Significado                                                                                                                                                                 |
    |---------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **CLSID**     | REG \_ SZ    | Cadena que contiene el identificador de clase COM de la clase auxiliar.                                                                                                            |
    | **Versión**   | REG \_ SZ    | Cadena que contiene las versiones principales y secundarias de la clase auxiliar con el formato &lt; principal &gt; &lt; secundaria &gt; .                                                        |
    | **Publicado** | REG \_ DWORD | Un valor de 1 significa que se espera que esta clase auxiliar se invoque directamente desde el cliente de Diagnostics. 0 significa que solo se puede llamar desde otra clase auxiliar. |
    | **Parent**    | REG \_ SZ    | Cadena que denomina la clase auxiliar extensible de Microsoft que se está ampliando.                                                                                       |

    

     

3.  Para cada clase auxiliar, publique la lista de atributos correspondientes mediante la creación de una clave en

    **HKLM \\ System \\ CurrentControlSet \\ Control \\ NetDiagFx** \\ *VendorName* \\ **HostDLLs** \\ *Helper Class* \\ **HelperClasses** \\ *Helper Class Name* \\ **MatchAttributes**

    La clave debe contener uno o varios valores (uno por atributo) del tipo siguiente.

    | Valor             | Tipo                             | Significado                                                                    |
    |-------------------|----------------------------------|----------------------------------------------------------------------------|
    | **AttributeName** | REG \_ SZ \| REG \_ DWORD \| REG \_ BINARY | Valor que completa el par de nombre y valor de un atributo determinado. |

    

     

 

 




