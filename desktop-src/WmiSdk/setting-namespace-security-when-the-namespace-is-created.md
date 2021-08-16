---
title: Establecimiento de la seguridad en la creación de espacios de nombres
description: El Managed Object Format (MOF) que crea un espacio de nombres también puede definir los descriptores de seguridad para el espacio de nombres incluyendo el calificador NamespaceSecuritySDDL con el descriptor de seguridad en formato sddl (lenguaje de definición de descriptores de seguridad).
ms.assetid: eeda3351-11ec-4064-90dd-f67ccf5c8cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 004e1897553ef2ec0bd57067b17d714f6aaf8b17059c1078a2fc0da8a060a40f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118315642"
---
# <a name="setting-security-on-namespace-creation"></a>Establecimiento de la seguridad en la creación de espacios de nombres

El Managed Object Format (MOF) que crea un espacio de nombres también puede definir los descriptores de seguridad para el espacio de nombres incluyendo el calificador **NamespaceSecuritySDDL** con el descriptor de seguridad en formato [sddl (lenguaje](/windows/desktop/SecAuthZ/security-descriptor-definition-language) de definición de [*descriptores*](/windows/desktop/SecGloss/s-gly) de seguridad).

Puede usar **NamespaceSecuritySDDL para** proteger cualquier espacio de nombres. También puede usar este calificador en un archivo MOF simple para modificar el descriptor de seguridad en un espacio de nombres existente. WMI procesa la cadena SDDL para establecer la seguridad del espacio de nombres, pero no se almacena como una cadena. Si no se especifica ningún descriptor de seguridad, se usa la seguridad predeterminada. Para obtener más información, vea [Setting Namepace Security Descriptors](setting-namespace-security-descriptors.md).

El procedimiento siguiente establece el descriptor de seguridad para el *espacio \\ de nombres MyNamespace* raíz. La cadena SDDL establece el propietario y el grupo en usuarios autenticados y especifica una lista de control de acceso discrecional [*(DACL)*](/windows/desktop/SecGloss/d-gly) heredada por espacios de nombres secundarios. La DACL permite al usuario el derecho de leer datos, ejecutar métodos, escribir datos en clases de proveedor y usar el acceso remoto: **WBEM \_ ENABLE**, **WBEM \_ METHOD \_ EXECUTE**, **WBEM \_ WRITE \_ PROVIDER** y **WBEM REMOTE \_ \_ ACCESS**. Para obtener más información, vea [Acceso a espacios de nombres WMI.](access-to-wmi-namespaces.md)

**Para establecer una DACL de espacio de nombres**

1.  Cree un archivo Managed Object Format (MOF) o modifique el archivo MOF existente que defina el espacio de nombres para agregar el calificador **NamespaceSecuritySDDL** con la cadena SDDL.

    En el ejemplo de código siguiente se muestra que el espacio de nombres que se va a modificar es root MyNamespace y el archivo \\ se denomina MyNamespace \_ security.mof.

    ```mof
    #pragma autorecover
    #pragma namespace("\\\\.\\root")
    [NamespaceSecuritySDDL ("O:BAG:BAD:(A;CI;0x60003;;;WD)")]
    Instance of __Namespace
    {
      Name = "MyNamespace";
    };
    ```

    

2.  Tenga en cuenta que la cadena SDDL distingue mayúsculas de minúsculas: las letras deben escribirse en mayúsculas.

    En el ejemplo de código siguiente se muestran las letras "o" y "g" en la cadena SDDL como minúsculas y hará que Mofcomp.exe devuelva un error.

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

    **c: \\ mofcomp MyNamespace \_ security.mof**

    En C++, use los [**métodos IMoFCompiler.**](/windows/desktop/api/Wbemcli/nn-wbemcli-imofcompiler)

4.  Si se produce un error en el intento de establecer el espacio de nombres DACL, tenga en cuenta los siguientes mensajes de error:

    

    | Error                           | Descripción                                                                                                  |
    |---------------------------------|--------------------------------------------------------------------------------------------------------------|
    | **WBEM \_ E \_ INVALID \_ PARAMETER** | No hay ninguna DACL heredada. Como alternativa, el autor de la llamada ha infringido la DACL o la SD en el espacio de nombres primario. |
    | **WBEM \_ E \_ ACCESS \_ DENIED**     | El autor de la llamada no tiene permiso para actualizar el SDDL en MOF.                                               |

    

     

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Establecer descriptores de seguridad de espacio de nombres](setting-namespace-security-descriptors.md)
</dt> <dt>

[**Constantes de derechos de acceso de espacio de nombres**](namespace-access-rights-constants.md)
</dt> <dt>

[**Constantes de marca ACE de espacio de nombres**](namespace-ace-flag-constants.md)
</dt> <dt>

[Cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
