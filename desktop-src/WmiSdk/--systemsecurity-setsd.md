---
description: Establece el descriptor de seguridad del espacio de nombres al que está conectado un usuario. Este método requiere un descriptor de seguridad en formato binario de matriz de bytes. Si va a escribir un script, use el método SetSecurityDescriptor.
ms.assetid: 049f8722-1674-4c4f-9300-09b1cc1412fb
ms.tgt_platform: multiple
title: Método SetSD de la __SystemSecurity clase
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
ms.openlocfilehash: 04da59b6370e2e9a381f2e3889b75ac37cb926e54c46cc0e616ec5353ed6f665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132038"
---
# <a name="setsd-method-of-the-__systemsecurity-class"></a>Método SetSD de la \_ \_ clase SystemSecurity

El **método SetSD** establece el descriptor de seguridad para el espacio de nombres al que está conectado un usuario. Este método requiere un descriptor de seguridad en formato binario de matriz de bytes. Si va a escribir un script, use el [**método SetSecurityDescriptor.**](setsecuritydescriptor-method-in-class---systemsecurity.md) Para obtener más información, vea [Proteger espacios de nombres WMI y](securing-wmi-namespaces.md) Cambiar la seguridad de acceso en objetos [protegibles.](changing-access-security-on-securable-objects.md)

Si está programando en C++, puede manipular el descriptor de seguridad binario mediante [SDDL](/windows/desktop/SecAuthZ/security-descriptor-definition-language)y los métodos de conversión [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) y [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).

Un usuario debe tener el **permiso WRITE \_ DAC** y, de forma predeterminada, un administrador tiene ese permiso. La única parte del descriptor de seguridad que se usa es la entrada de control de acceso no incluido (ACE) en la lista de control de acceso discrecional (DACL). Al establecer la **marca CONTAINER \_ INHERIT** en las ACE, el descriptor de seguridad afecta a los espacios de nombres secundarios. Se permiten tanto las ACE de permiso como las de denegación.

> [!Note]  
> Dado que tanto deny como allow ACE se permiten en una DACL, el orden de las ACE es importante. Para obtener más información, vea [Ordenación de AEE en una DACL.](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)

 

## <a name="syntax"></a>Sintaxis


```mof
HRESULT SetSD(
  [in] uint8 SD[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SD* \[ En\]
</dt> <dd>

Matriz de bytes que forma el descriptor de seguridad.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT** que indica el estado de una llamada de método. Para scripting y Visual Basic aplicaciones, el resultado se puede obtener de [OutParameters.ReturnValue](parsing-outparameters-objects.md). Para obtener más información, [vea Construir objetos InParameters y Analizar objetos OutParameters](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

En la lista siguiente se enumeran los valores devueltos que son **significativos para SetSD.**

<dl> <dt>

**S \_ OK**
</dt> <dd>

El método se ejecutó correctamente.

</dd> <dt>

**WBEM \_ E \_ ACCESS \_ DENIED**
</dt> <dd>

El autor de la llamada no tiene derechos suficientes para llamar a este método.

</dd> <dt>

**MÉTODO WBEM \_ E \_ \_ DESHABILITADO**
</dt> <dd>

Se intentó ejecutar este método en un sistema operativo que no lo admite.

</dd> <dt>

**WBEM \_ E \_ INVALID \_ OBJECT**
</dt> <dd>

SD no supera las pruebas de validez básicas.

</dd> <dt>

**WBEM \_ E \_ INVALID \_ PARAMETER**
</dt> <dd>

SD no es válido debido a uno de los siguientes elementos:

-   Falta DACL.
-   DACL no es válida.
-   ACE tiene establecida **la marca WBEM \_ FULL WRITE \_ \_ REP** y no se ha establecido la marca **WBEM PARTIAL WRITE \_ \_ \_ REP** o **WBEM WRITE \_ \_ PROVIDER.**
-   ACE tiene la **marca ACE INHERIT \_ ONLY \_** establecida sin la **marca ACE CONTAINER \_ INHERIT. \_**
-   ACE tiene un conjunto de bits de acceso desconocido.
-   ACE tiene un conjunto de marcas que no está en la tabla.
-   ACE tiene un tipo que no está en la tabla.
-   Falta el propietario y el grupo en la SD.

Para obtener más información sobre las marcas de entrada de control de acceso (ACE), vea [Wmi Security Constants](wmi-security-constants.md).

</dd> </dl>

## <a name="remarks"></a>Comentarios

Para obtener más información sobre cómo modificar la seguridad del espacio de nombres mediante programación o manualmente, vea [Securing WMI Namespaces](securing-wmi-namespaces.md).

## <a name="examples"></a>Ejemplos

El siguiente script muestra cómo usar **SetSD** para establecer el descriptor de seguridad del espacio de nombres para el espacio de nombres raíz y cambiarlo a la matriz de bytes que se muestra *en strSD*.


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



El siguiente ejemplo de código de C# usa System.Security.AccessControl.RawSecurityDescriptor para enumerar, insertar y quitar nuevos objetos CommonAce en RawSecurityDescriptor.DiscretionaryAcl y, a continuación, convertirlos de nuevo en una matriz de bytes para guardarlos a través de SetSD. SecurityIdentifier se puede recuperar mediante NTAccount y Translate.


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

[**\_\_SystemSecurity::GetSD**](--systemsecurity-getsd.md)
</dt> <dt>

[Constantes de seguridad wmi](wmi-security-constants.md)
</dt> <dt>

[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
</dt> <dt>

[**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
</dt> <dt>

[Protección de espacios de nombres WMI](securing-wmi-namespaces.md)
</dt> </dl>

 

