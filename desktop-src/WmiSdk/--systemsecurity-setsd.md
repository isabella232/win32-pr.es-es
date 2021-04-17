---
description: Establece el descriptor de seguridad para el espacio de nombres al que está conectado un usuario. Este método requiere un descriptor de seguridad en formato binario de matriz de bytes. Si está escribiendo un script, use el método SetSecurityDescriptor.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Método establecido de la clase __SystemSecurity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __SystemSecurity.SetSD
api_type:
- COM
api_location:
- All
ms.openlocfilehash: 21f09a412a662cec8629fa9237d8dbb5902426c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687694"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a>Método establecido de la \_ \_ clase SystemSecurity

El método **sets** establece el descriptor de seguridad para el espacio de nombres al que está conectado un usuario. Este método requiere un descriptor de seguridad en formato binario de matriz de bytes. Si está escribiendo un script, use el método [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) . Para obtener más información, vea [proteger los espacios de nombres WMI](securing-wmi-namespaces.md) y [cambiar la seguridad de acceso en objetos protegibles](changing-access-security-on-securable-objects.md).

Si está programando en C++, puede manipular el descriptor de seguridad binario mediante [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)y los métodos de conversión [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Un usuario debe tener el permiso **escribir \_ DAC** y, de forma predeterminada, un administrador tiene ese permiso. La única parte del descriptor de seguridad que se usa es la entrada de control de acceso (ACE) no heredada en la lista de control de acceso discrecional (DACL). Al establecer la marca de **\_ herencia de contenedor** en las ACE, el descriptor de seguridad afecta a los espacios de nombres secundarios. Se permiten las ACE de permitir y denegar.

> [!Note]  
> Dado que las ACE deny y Allow se permiten en una DACL, el orden de las ACE es importante. Para obtener más información, vea [ordenación de ACE en una DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).

 

## <a name="syntax"></a>Sintaxis


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SD* \[ de\]
</dt> <dd>

Matriz de bytes que constituye el descriptor de seguridad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT** que indica el estado de una llamada al método. En el caso de las aplicaciones de scripting y Visual Basic, el resultado se puede obtener de [Parameters. ReturnValue](parsing-outparameters-objects.md). Para obtener más información, consulte [construir objetos Parameters y analizar objetos Parameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

En la lista siguiente se enumeran los valores devueltos que son significativos para los **conjuntos**.

<dl> <dt>

**S \_ correcto**
</dt> <dd>

El método se ejecutó correctamente.

</dd> <dt>

**WBEM \_ E \_ acceso \_ denegado**
</dt> <dd>

El autor de la llamada no tiene derechos suficientes para llamar a este método.

</dd> <dt>

**WBEM \_ E \_ método \_ deshabilitado**
</dt> <dd>

Se intentó ejecutar este método en el sistema operativo que no lo admite.

</dd> <dt>

**\_ \_ objeto no válido de WBEM E \_**
</dt> <dd>

SD no pasa las pruebas de validez básicas.

</dd> <dt>

**\_ \_ parámetro no válido de WBEM E \_**
</dt> <dd>

SD no es válido debido a uno de los siguientes motivos:

-   Falta DACL.
-   DACL no válida.
-   ACE tiene establecida la marca de representador de **\_ \_ escritura completa \_ de WBEM** y no se ha establecido la marca de proveedor de escritura de WBEM o de **\_ \_ proveedor** de escritura WBEM **\_ \_ \_** .
-   ACE tiene la **marca \_ \_ ACE de solo heredar** establecida sin la marca de la **\_ \_ ACE de herencia de contenedor** .
-   ACE tiene un conjunto de bits de acceso desconocido.
-   ACE tiene un conjunto de marcas que no está en la tabla.
-   La ACE tiene un tipo que no está en la tabla.
-   Faltan el propietario y el grupo en SD.

Para obtener más información sobre las marcas de entrada de control de acceso (ACE), consulte [constantes de seguridad de WMI](wmi-security-constants.md).

</dd> </dl>

## <a name="remarks"></a>Observaciones

Para obtener más información sobre cómo modificar la seguridad de los espacios de nombres mediante programación o manualmente, consulte protección de los [espacios de nombres WMI](securing-wmi-namespaces.md).

## <a name="examples"></a>Ejemplos

En el script siguiente se muestra cómo **usar** seted para establecer el descriptor de seguridad del espacio de nombres para el espacio de nombres raíz y cambiarlo a la matriz de bytes que se muestra en *strSD*.


```VB
' Hard-coded security descriptor
strSD = array( 1, 0, 4,129,72, 0, 0, 0, _ 
              88, 0, 0,  0, 0, 0, 0, 0, _
              20, 0, 0,  0, 2, 0,52, 0, _
               2, 0, 0,  0, 0, 2,24, 0, _
              63, 0, 6,  0, 1, 2, 0, 0, _
               0, 0, 0,  5,32, 0, 0, 0, _
              32, 2, 0,  0, 0, 2,20, 0, _
              63, 0, 6,  0, 1, 1, 0, 0, _
               0, 0, 0,  1, 0, 0, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0, _
               1, 2, 0,  0, 0, 0, 0, 5, _
              32, 0, 0,  0,32, 2, 0, 0)

' Connect to WMI and the root namespace.
Set oSvc = CreateObject( _
                         "WbemScripting.SWbemLocator"). _
                         ConnectServer(,"Root\Cimv2")

' Get the single __SystemSecurity object in this namespace.
Set oSecurity = oSvc.Get("__SystemSecurity=@")

' Change the namespace security.
nReturn = oSecurity.SetSD(strSD)
WScript.Echo "ReturnValue " & nReturn
```



En el siguiente ejemplo de código de C# se usa System. Security. AccessControl. RawSecurityDescriptor para enumerar, insertar y quitar nuevos objetos CommonAce en RawSecurityDescriptor. DiscretionaryAcl y, a continuación, volver a convertirlos en una matriz de bytes para guardarlos a través de establecido. Un SecurityIdentifier se puede recuperar mediante NTAccount y translate.


```CSharp
 byte[] sdValueByteArray = new Byte[0];

            string accountName = "My User or Group";

            AceFlags aceFlags = AceFlags.ContainerInherit;

            int accessRights = 131107; // Search for Namespace Access Rights Constants and build an Flags enum

            RawSecurityDescriptor rawSecurityDescriptor = new RawSecurityDescriptor(sdValueByteArray, 0);

            NTAccount ntAccount = new NTAccount(accountName);

            IdentityReference identityReference = ntAccount.Translate(typeof(SecurityIdentifier));

            if (identityReference == null)

            {

                string message = string.Format("The IdentityReference of NTAccount '{0}' is null.", accountName);

                throw new Exception(message);

            }

            SecurityIdentifier securityIdentifier = identityReference as SecurityIdentifier;

            if (securityIdentifier == null)

            {

                string message = "The IdentityReference of NTAccount '{0}' is not an SecurityIdentifier.";

                throw new Exception(message);

            }

            CommonAce commonAce;

            foreach (GenericAce genericAce in rawSecurityDescriptor.DiscretionaryAcl)

            {

                commonAce = genericAce as CommonAce;

                if (commonAce == null)

                {

                    continue;

                }

                if (commonAce.SecurityIdentifier.Value.Equals(securityIdentifier.Value, StringComparison.OrdinalIgnoreCase))

                {

                    return;

                }

            }

            commonAce = new CommonAce(aceFlags, AceQualifier.AccessAllowed, (int)accessRights, securityIdentifier, false, null);

            rawSecurityDescriptor.DiscretionaryAcl.InsertAce(rawSecurityDescriptor.DiscretionaryAcl.Count, commonAce);

```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>       |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/> |
| Espacio de nombres<br/>                | Todos los espacios de nombres WMI<br/>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Clases del sistema WMI](wmi-system-classes.md)
</dt> <dt>

[**\_\_SystemSecurity**](--systemsecurity.md)
</dt> <dt>

[**\_\_SystemSecurity:: obtiene**](--systemsecurity-getsd.md)
</dt> <dt>

[Constantes de seguridad de WMI](wmi-security-constants.md)
</dt> <dt>

[**ACE de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**SecurityDescriptor de Win32 \_**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Proteger los espacios de nombres de WMI](securing-wmi-namespaces.md)
</dt> </dl>

 

