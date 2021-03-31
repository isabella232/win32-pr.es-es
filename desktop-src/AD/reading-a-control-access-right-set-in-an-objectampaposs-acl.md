---
title: Leer un conjunto derecho de control de acceso en la ACL de un objeto
description: Las propiedades de la interfaz IADsAccessControlEntry se usan para conceder o denegar derechos de acceso de control.
ms.assetid: 2c6fef91-990e-4954-9aff-c9ec72d13972
ms.tgt_platform: multiple
keywords:
- Leer un conjunto de derechos de acceso de control en la ACL de un objeto Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877c96a95fc94095c79ad129e8a07b1c786abe1
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077503"
---
# <a name="reading-a-control-access-right-set-in-an-objects-acl"></a>Leer un conjunto derecho de control de acceso en la ACL de un objeto

Con ADSI, se lee una ACE de derechos de control de acceso igual que cualquier otra ACE de una ACL. Tenga en cuenta que también puede usar las API de seguridad de Win32 para leer ACL en objetos de directorio. Sin embargo, los derechos de acceso de control utilizan las propiedades de la interfaz [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) de una manera específica para conceder y denegar derechos de acceso de control:

-   [**AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) debe contener **\_ el \_ acceso de \_ control \_ DS adecuado de ADS**.
-   El valor de [**Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) es el **tipo de objeto de \_ marca ADS \_ \_ \_ presente**.
-   [**Objecttype**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) es la forma de cadena del atributo **rightsGUID** del derecho de acceso de control. El formato de cadena del GUID es el mismo que el de la función de biblioteca com [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) .
-   [**AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) es el **objeto de ADS \_ AceType \_ Access \_ \_ allowed** , para conceder al administrador de confianza el derecho de acceso de control o **ADS \_ AceType \_ acceso \_ denegado \_** para denegar al administrador de confianza el derecho de acceso de control.
-   [**Trustee**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) es la entidad de seguridad; es el usuario, el grupo, el equipo, etc., al que se aplica la ACE.

Utilice el procedimiento siguiente para leer una ACE para un objeto ADSI. El siguiente procedimiento se aplica a las aplicaciones de C y C++.

**Para leer una ACE para un objeto ADSI**

1.  Obtiene un puntero de interfaz [**IADs**](/windows/desktop/api/iads/nn-iads-iads) al objeto.
2.  Use el método [**IADs:: get**](/windows/desktop/api/iads/nf-iads-iads-get) para obtener el descriptor de seguridad del objeto. El nombre de la propiedad que contiene el descriptor de seguridad es "nTSecurityDescriptor". La propiedad se devolverá como una **variante** que contiene un puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Tenga en cuenta que el miembro de **VT** es el **\_ envío de VT**. Llame a **QueryInterface** en ese puntero **IDispatch** para obtener una interfaz [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) para usar los métodos de esa interfaz para tener acceso a la ACL del descriptor de seguridad.
3.  Use el método [**IADsSecurityDescriptor:: get \_ DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) para obtener la ACL. El método devuelve un puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Llame a **QueryInterface** en ese puntero **IDispatch** para obtener una interfaz [**IADsAccessControlList**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrollist) para usar los métodos de esa interfaz para tener acceso a las ACE individuales de la ACL.
4.  Use el método [**IADsAccessControlList:: get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadsaccesscontrollist-get__newenum) para enumerar las ACE. El método devuelve un puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . Llame a **QueryInterface** en ese puntero **IUnknown** para obtener una interfaz [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) .
5.  Use el método [**IEnumVARIANT:: Next**](/windows/win32/api/oaidl/nf-oaidl-ienumvariant-next) para enumerar las ACE de la ACL. La propiedad se devuelve como un **valor de tipo Variant** que contiene un puntero [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . Tenga en cuenta que el miembro de **VT** es el **\_ envío de VT**. Llame a **QueryInterface** en ese puntero **IDispatch** para obtener una interfaz [**IADsAccessControlEntry**](/windows/desktop/api/iads/nn-iads-iadsaccesscontrolentry) para leer la ACE.
6.  Llame al [**método IADsAccessControlEntry:: \_ Get AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para obtener la **AccessMask** y compruebe que el valor de **AccessMask** para la marca de **\_ \_ \_ \_ acceso de control DS** de ad derecho de ADS. Si tiene esta marca, la ACE contiene un derecho de acceso de control.
7.  Llame al método [**IADsAccessControlEntry:: get \_ Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para obtener la marca para el tipo de objeto.
8.  Valor de [**marcas**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) check para la marca present del **tipo de \_ \_ objeto de \_ \_ marca ADS** . Si **Flags** se establece en **ADS \_ Flag Type (tipo de \_ objeto \_ \_**), llame al método **IADsAccessControlEntry:: get \_ objecttype** para obtener una cadena que contenga el rightsGUID del derecho de acceso de control al que se aplica la ACE.
9.  Llame al método [**IADsAccessControlEntry:: get \_ AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para obtener el tipo de ACE. El tipo será un **\_ \_ \_ \_ objeto permitido de ADS ACETYPE** para conceder al administrador de confianza el derecho de acceso de control o **ADS \_ ACETYPE \_ acceso \_ denegado \_** para denegar el derecho de acceso de control.
10. Llame al método [**IADsAccessControlEntry:: get \_ Trustee**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) para obtener la entidad de seguridad; es decir, usuario, grupo, equipo y así sucesivamente al que se aplica la ACE.
11. Cuando termine con las cadenas [**objecttype**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) y **Trustee** , utilice [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) para liberar la memoria de esas cadenas.
12. Cuando termine con las interfaces, llame a **Release** para disminuir o liberar todas las referencias de interfaz.

 

 