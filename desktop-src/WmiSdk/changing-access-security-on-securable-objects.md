---
description: A partir Windows Vista, muchos objetos protegibles tienen métodos para obtener o establecer el descriptor de seguridad. Con los permisos adecuados, puede leer o cambiar descriptores de seguridad en objetos protegibles.
ms.assetid: da660e7e-f32d-4b7d-b979-f7b482a73fa2
ms.tgt_platform: multiple
title: Cambiar la seguridad de acceso en objetos protegibles
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e4cdaa948e6f0e695b3e77576b0a0726f0b38f3b649f005b42aa8e205c894db8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050993"
---
# <a name="changing-access-security-on-securable-objects"></a>Cambiar la seguridad de acceso en objetos protegibles

Las impresoras, los servicios, las claves del Registro, las aplicaciones DCOM y los espacios de nombres WMI son objetos protegibles. El acceso a objetos protegibles está protegido por [*descriptores de seguridad*](/windows/desktop/SecGloss/s-gly), que especifican los usuarios que tienen acceso. A partir Windows Vista, muchos objetos protegibles tienen métodos para obtener o establecer el descriptor de seguridad. Con los permisos adecuados, puede leer o cambiar descriptores de seguridad en objetos protegibles. Con estos métodos, puede controlar qué cuentas de usuario o grupos tienen acceso a una impresora, servicio, espacio de nombres WMI u otro objeto. Para obtener más información sobre los descriptores de seguridad y su uso en WMI, vea Acceso a [objetos protegibles de WMI.](access-to-wmi-securable-objects.md)

En este tema se de abordan las siguientes secciones:

-   [Objetos y métodos descriptores de seguridad](#objects-and-security-descriptor-methods)
-   [Conversión entre formatos de descriptor de seguridad](#converting-between-security-descriptor-formats)
-   [Problemas de seguridad](#security-issues)
-   [Temas relacionados](#related-topics)

## <a name="objects-and-security-descriptor-methods"></a>Objetos y métodos descriptores de seguridad

La lista siguiente contiene los métodos que los objetos protegibles tienen para permitirle leer o cambiar el descriptor de seguridad:

-   Espacios de nombres WMI

    Un proveedor puede establecer una seguridad que solo permita que determinados grupos tengan acceso a los datos de un espacio de nombres WMI. La seguridad del espacio de nombres se controla mediante métodos de [**\_ \_ la clase SystemSecurity.**](--systemsecurity.md) A partir Windows Vista, los [**métodos GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) y [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) devuelven y escriben [**\_ \_ objetos SecurityDescriptor.**](--securitydescriptor.md) Para obtener más información, vea [Establecer descriptores de seguridad de espacio de nombres](setting-namespace-security-descriptors.md).

-   Claves del Registro

    A partir Windows Vista, puede proteger las claves del Registro para que no las puedan cambiar usuarios no autorizados. La [**clase StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) tiene los [**métodos GetSecurityDescriptor**](/previous-versions/windows/desktop/regprov/getsecuritydescriptor-method-in-class-stdregprov) [**y SetSecurityDescriptor.**](/previous-versions/windows/desktop/regprov/setsecuritydescriptor-method-in-class-stdregprov) Estos métodos devuelven y [**escriben objetos \_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

-   Impresoras

    A partir Windows Vista, puede proteger el acceso a las instancias de la clase Printer de [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-printer) mediante los métodos [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) y [**SetSecurityDescriptor.**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-printer) Estos métodos devuelven y [**escriben objetos \_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

-   Servicios

    A partir Windows Vista, puede proteger el acceso a las instancias de la clase De servicio [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service) mediante los métodos [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) y [**SetSecurityDescriptor.**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) Estos métodos devuelven y [**escriben objetos \_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

-   Aplicaciones DCOM

    Las instancias de aplicación DCOM tienen varios descriptores de seguridad. A partir Windows Vista, use métodos de la clase [**\_ DCOMApplicationSetting de Win32**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting) para obtener o cambiar los distintos descriptores de seguridad. Los descriptores de seguridad se devuelven como instancias de la [**clase \_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

    Para obtener o cambiar los permisos de configuración, llame a los [**métodos GetConfigurationSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting) [**o SetConfigurationSecurityDescriptor.**](/windows/desktop/CIMWin32Prov/setconfigurationsecuritydescriptor-method-in-class-win32-dcomapplicationsetting)

    Para obtener o cambiar los permisos de acceso, llame a los métodos [**GetAccessSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting) [**o SetAccessSecurityDescriptor.**](/windows/desktop/CIMWin32Prov/setaccesssecuritydescriptor-method-in-class-win32-dcomapplicationsetting)

    Para obtener o cambiar los permisos de inicio y activación, llame a los [**métodos GetLaunchSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getlaunchsecuritydescriptor-in-class-win32-dcomapplicationsetting) o [**SetLaunchSecurityDescriptor.**](/windows/desktop/CIMWin32Prov/setlaunchsecuritydescriptor-method-in-class-win32-dcomapplicationsetting)

-   Files

    Los [**métodos GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) y [**SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalfilesecuritysetting) están en la clase [**\_ LogicalFileSecuritySetting de Win32,**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalfilesecuritysetting) en lugar de en la [**clase \_ DataFile de CIM.**](/windows/desktop/CIMWin32Prov/cim-datafile)

-   Recursos compartidos

    Los [**métodos GetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/getsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) y [**SetSecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/setsecuritydescriptor-method-in-class-win32-logicalsharesecuritysetting) están en la clase [**\_ LogicalShareSecuritySetting de Win32,**](/previous-versions/windows/desktop/secrcw32prov/win32-logicalsharesecuritysetting) en lugar de en la [**clase Win32 \_ Share.**](/windows/desktop/CIMWin32Prov/win32-share)

> [!Note]  
> Cuando no se especifica una nueva lista de Access Control seguridad [*(SACL)*](/windows/desktop/SecGloss/s-gly) en una llamada a un método **SetSecurityDescriptor,** el descriptor de seguridad SACL del objeto protegible de destino se establece en **NULL** para que la configuración sacl anterior no se conserve.

 

## <a name="converting-between-security-descriptor-formats"></a>Conversión entre formatos de descriptor de seguridad

Los descriptores de seguridad son matrices de bytes binarios complejas que normalmente se deben crear y cambiar en C++. Después de usar uno de los métodos Get para obtener el descriptor de seguridad, la clase [**\_ SecurityDescriptorHelper de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) proporciona métodos que convierten descriptores de seguridad en lenguaje de definición de descriptores de seguridad [(SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language) o en instancias de [**\_ SecurityDescriptor de Win32.**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)

Puede manipular las listas de Access Control (ACL) más fácilmente en instancias [**\_ de SecurityDescriptor de Win32**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) o en SDDL. Para obtener más información sobre la estructura y el uso de descriptores de seguridad en WMI, vea [Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md).

En C++ o C# use funciones de conversión para convertir descriptores de seguridad binarios en lenguaje de definición de descriptores de [seguridad (SDDL).](/windows/desktop/SecAuthZ/security-descriptor-definition-language) Para modificar los valores del descriptor de seguridad en aplicaciones de C++, use [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

## <a name="security-issues"></a>Problemas de seguridad

Se recomienda que los cambios en los descriptores de seguridad se realicen con mucha precaución para que la seguridad del objeto no se vea comprometida. Tenga en cuenta que el orden de las entradas de control de acceso (ACE) en una lista de control de acceso discrecional (DACL) puede afectar a la seguridad de acceso. Para obtener más información, [vea Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Objetos de descriptor de seguridad WMI](wmi-security-descriptor-objects.md)
</dt> <dt>

[Clase auxiliar del descriptor de seguridad](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[Procedimientos recomendados de seguridad](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[Mantener la seguridad de WMI](maintaining-wmi-security.md)
</dt> <dt>

[Control de acceso](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[Acceso a espacios de nombres WMI](access-to-wmi-namespaces.md)
</dt> </dl>

 

 
