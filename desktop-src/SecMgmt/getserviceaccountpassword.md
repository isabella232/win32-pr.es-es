---
description: Recupera la contraseña de la cuenta de servicio.
ms.assetid: B3D3842F-ACEB-4979-B336-BA3D0143044C
title: Función GetServiceAccountPassword (Secpkg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetServiceAccountPassword
api_type:
- HeaderDef
api_location:
- Secpkg.h
ms.openlocfilehash: 08719fb2b7e4a775df890f20cd640d059cb44475
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105688026"
---
# <a name="getserviceaccountpassword-function"></a>GetServiceAccountPassword función)

Recupera la contraseña de la cuenta de servicio, disponible para los [*proveedores de compatibilidad para seguridad*](/windows/desktop/SecGloss/s-gly) (SSP), como Kerberos SSP.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS NTAPI GetServiceAccountPassword(
  _In_        PUNICODE_STRING AccountName,
  _In_opt_    PUNICODE_STRING DomainName,
  _In_        CRED_FETCH      CredFetch,
  _Inout_opt_ FILETIME        *FileTimeExpiry,
  _Out_       PUNICODE_STRING CurrentPassword,
  _Out_       PUNICODE_STRING PreviousPassword,
  _Out_opt_   FILETIME        *FileTimeCurrPwdValidForOutbound
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*AccountName* \[ de\]
</dt> <dd>

Nombre de cuenta terminada en NULL de la cuenta de la cuenta de servicio administrada de grupo (gMSA). El nombre de usuario puede ser uno de los siguientes formatos:

-   Nombre de cuenta SAM del gMSA.
-   Nombre de usuario en un nombre de dominio completo (FQDN), como *domainname * **\\** _username_ o **www.** _dominio_* de _. com \\_ * _nombre_. El nombre de usuario debe ser un nombre de SAM únicamente. El nombre de dominio puede ser un nombre DNS o un nombre NetBIOS.
-   Nombre principal de usuario (UPN) implícito para la cuenta de gMSA, por ejemplo, *SomeName * **@** _Domain_*_. com_*, donde, según la definición de un UPN implícito, el *dominio * * *. com** es el nombre DNS real del dominio.

</dd> <dt>

*Dominio* \[ de en, opcional\]
</dt> <dd>

Nombre de dominio opcional terminado en NULL. Esto solo es válido si el parámetro *AccountName* es un nombre de cuenta SAM. El nombre de dominio solo puede ser un nombre NetBIOS o un nombre de dominio completo (FQDN).

</dd> <dt>

*CredFetch* \[ de\]
</dt> <dd>

Un valor de la enumeración [**CRED \_ Fetch**](cred-fetch.md) que especifica cómo recuperar la credencial.



| Value                                                                                                                                                                                                    | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CredFetchDefault"></span><span id="credfetchdefault"></span><span id="CREDFETCHDEFAULT"></span><dl> <dt>**CredFetchDefault**</dt> </dl> | El sistema operativo primero intenta recuperar la contraseña de la memoria caché local si no es hora de capturar la contraseña. Si es el momento de capturar la contraseña, el sistema operativo se pone en contacto con el controlador de dominio; de lo contrario, devuelve cualquier contraseña almacenada en caché con un valor de estado correcto.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="CredFetchDPAPI"></span><span id="credfetchdpapi"></span><span id="CREDFETCHDPAPI"></span><dl> <dt>**CredFetchDPAPI**</dt> </dl>         | Devuelve la credencial DPAPI local al autor de la llamada. Los SSP generalmente no requieren el uso de este valor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="CredFetchForced"></span><span id="credfetchforced"></span><span id="CREDFETCHFORCED"></span><dl> <dt>**CredFetchForced**</dt> </dl>     | Obliga al sistema operativo a intentar leer la contraseña del controlador de dominio. Durante el tiempo de sustitución de contraseña, la contraseña puede haber cambiado en el controlador de dominio y en otros hosts miembros, pero el host miembro gMSA reconoce la contraseña como todavía válida. Esto puede ocurrir debido a problemas de sesgo del reloj entre distintos controladores de dominio. Cuando se especifica este valor, el sistema operativo determina si puede haber un posible cambio de contraseña debido al sesgo del reloj y, en caso afirmativo, recupera la contraseña. De lo contrario, se devuelve la credencial almacenada en caché. Si no hay ninguna credencial almacenada en caché, el sistema operativo intenta obtener una del controlador de dominio.<br/> |



 

</dd> <dt>

*FileTimeExpiry* \[ in, out, opcional\]
</dt> <dd>

En la entrada, si este valor no es NULL y no es un **FILETIME** de cero, *FileTimeExpiry* contiene la hora de expiración de las credenciales de la cuenta de servicio que conoce el autor de la llamada. Si el parámetro *FileTimeExpiry* es el mismo que el de una de las credenciales actuales, se produce un error en esta llamada. En la salida, el parámetro *FileTimeExpiry* contiene la hora de expiración de la credencial que se va a devolver.

</dd> <dt>

*CurrentPassword* \[ enuncia\]
</dt> <dd>

La contraseña actual de gMSA.

</dd> <dt>

*PreviousPassword* \[ enuncia\]
</dt> <dd>

La contraseña anterior de gMSA.

</dd> <dt>

*FileTimeCurrPwdValidForOutbound* \[ out, opcional\]
</dt> <dd>

Denota el tiempo después del cual la contraseña actual es válida para las solicitudes salientes. El autor de la llamada debe comparar la hora actual con este valor y usar la contraseña actual devuelta solo si la hora actual es mayor o igual que el valor devuelto por este parámetro. El uso de este parámetro está diseñado para llamadores que no tienen reintentos en la lógica de salida, por ejemplo, NTLM.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es STATUs \_ Success.

Si se produce un error en la función, el valor devuelto es un código NTSTATUS. Para obtener más información, vea [valores devueltos de la función de directiva LSA](management-return-values.md).

Puede usar la función [**LsaNtStatusToWinError**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsantstatustowinerror) para convertir el código NTSTATUS en un código de error de Windows.

Cuando haya terminado de usar los búferes devueltos en los parámetros *CurrentPassword* y *PreviousPassword* , liberelos mediante una llamada a la función [**FreeLsaHeap**](/windows/desktop/api/ntlsa/nc-ntlsa-lsa_free_lsa_heap) .

## <a name="remarks"></a>Observaciones

Se puede llamar a la función **GetServiceAccountPassword** en los escenarios siguientes:

-   En las funciones de inicio de sesión de los proveedores de compatibilidad para seguridad (SSP), el SSP debe detectar que la contraseña de la cuenta de servicio \_ \_ se utiliza para iniciar sesión en la entidad y debe comprobar que el autor de la llamada tiene privilegios TCB o es un servicio de red. Después, el SSP debe permitir que el proceso de inicio de sesión continúe obteniendo la credencial más reciente mediante una llamada a la función **GetServiceAccountPassword** con el valor **CredFetchDefault** en la enumeración de [**\_ recopilación de credenciales**](cred-fetch.md) .

-   Desde SSP en sus llamadas [**InitializeSecurityContext**](../SecAuthN/initializesecuritycontext--general.md) y [**AcceptSecurityContext**](../SecAuthN/acceptsecuritycontext--general.md) . Los SSP deben detectar que la \_ \_ contraseña de la cuenta de servicio se utiliza para estas llamadas y, si la llamada es para las credenciales no principales, el SSP debe asegurarse de que el autor de la llamada tenga privilegios TCB o sea un servicio de red. A continuación, el SSP debe llamar a la función **GetServiceAccountPassword** con el valor **CredFetchDefault** en la enumeración de [**\_ recopilación de credenciales**](cred-fetch.md) y continuar con la llamada. Si se produce un error en las llamadas a **InitializeSecurityContext** y **ACCEPTSECURITYCONTEXT** , el SSP debe usar el *FileTimeExpiry* recuperado de la llamada anterior a **GetServiceAccountPassword** y usarlo como entrada para llamar a **GetServiceAccountPassword** de nuevo con el valor **CredFetchForced** en la enumeración de **\_ recopilación de credenciales** . Si hay disponible una nueva credencial de gMSA, la segunda llamada se realizará correctamente con nuevas credenciales y el SSP debe volver a intentarlo con las nuevas credenciales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Secpkg. h</dt> </dl> |



 

