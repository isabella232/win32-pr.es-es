---
title: Establecer la seguridad en la creación de espacios de nombres
description: El archivo Managed Object Format (MOF) que crea un espacio de nombres también puede definir los descriptores de seguridad para el espacio de nombres incluyendo el calificador NamespaceSecuritySDDL con el descriptor de seguridad en el formato de lenguaje de definición de descriptores de seguridad (SDDL).
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 461b23dbac3984ffdd49311cbe340ae2b0c5b022
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546875"
---
# <a name="setting-security-on-namespace-creation"></a>Establecer la seguridad en la creación de espacios de nombres

El archivo Managed Object Format (MOF) que crea un espacio de nombres también puede definir los descriptores de [*seguridad*](/windows/desktop/SecGloss/s-gly) para el espacio de nombres incluyendo el calificador **NamespaceSecuritySDDL** con el descriptor de seguridad en el formato de [lenguaje de definición de descriptores de seguridad (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) .

Puede usar **NamespaceSecuritySDDL** para proteger cualquier espacio de nombres. También puede usar este calificador en un archivo MOF simple para modificar el descriptor de seguridad de un espacio de nombres existente. WMI procesa la cadena SDDL para establecer la seguridad del espacio de nombres, pero no se almacena como una cadena. Si no se especifica ningún descriptor de seguridad, se usa la seguridad predeterminada. Para obtener más información, consulte [configuración de descriptores de seguridad de espacio](setting-namespace-security-descriptors.md).

El siguiente procedimiento establece el descriptor de seguridad para el espacio de nombres de la *raíz \\* myNameSpace. La cadena SDDL establece el propietario y el grupo en usuarios autenticados y especifica una [*lista de control de acceso discrecional (DACL)*](/windows/desktop/SecGloss/d-gly) que heredan los espacios de nombres secundarios. La DACL permite al usuario leer datos, ejecutar métodos, escribir datos en clases de proveedor y usar el acceso remoto: **WBEM \_ enable**, **WBEM \_ Method \_ Execute**, **WBEM \_ Write \_ Provider**, WBEM **\_ Remote \_ Access**. Para obtener más información, vea [acceso a los espacios de nombres WMI](access-to-wmi-namespaces.md).

**Para establecer una DACL de espacio de nombres**

1.  Cree un archivo Managed Object Format (MOF) o modifique el archivo MOF existente que define el espacio de nombres para agregar el calificador **NamespaceSecuritySDDL** con la cadena SDDL.

    En el ejemplo de código siguiente se muestra que el espacio de nombres que se va a modificar es la raíz \\ myNameSpace y el archivo se denomina myNameSpace \_ Security. mof.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  Tenga en cuenta que la cadena SDDL distingue entre mayúsculas y minúsculas: las letras deben escribirse en mayúsculas.

    En el ejemplo de código siguiente se muestran las letras "o" y "g" en la cadena SDDL en minúsculas, lo que hará que Mofcomp.exe devuelva un error.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL("o:BAg:BAD:(A;CI;0x60003;;;WD)")] 
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

3.  Ejecute [**Mofcomp.exe**](mofcomp.md) para compilar el archivo MOF.

    **c: \\ MOFCOMP myNameSpace \_ Security. mof**

    En C++, utilice los métodos [**IMoFCompiler**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler) .

4.  Si se produce un error al intentar establecer la DACL del espacio de nombres, tenga en cuenta los siguientes mensajes de error:

    

    | Error                           | Descripción                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | **\_ \_ parámetro no válido de WBEM E \_** | No hay ninguna DACL heredada. Como alternativa, el autor de la llamada ha infringido la DACL o el SD en el espacio de nombres primario. |
    | **WBEM \_ E \_ acceso \_ denegado**     | El autor de la llamada no tiene permiso para actualizar el SDDL en MOF.                                               |

    

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de descriptores de seguridad de espacios de nombres](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Constantes de derechos de acceso de espacio de nombres**](namespace-access-rights-constants.md)
</dt> <dt>

[**Constantes de marca ACE de espacio de nombres**](namespace-ace-flag-constants.md)
</dt> <dt>

[Cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
