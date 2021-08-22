---
description: Permite a un cliente administrar la configuración de cuota global de disco de un volumen NTFS. Este objeto hace que la funcionalidad esencial de la interfaz DIDiskQuotaUser esté disponible para scripting y aplicaciones basadas Visual Basic Microsoft.
title: DiDiskQuotaUser, objeto
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 0cdf3293-3dcf-44e7-a80d-4eacf9d09fbf
ms.openlocfilehash: 65d8397ed07fc3ebab9fd4846b008f97c1b7e756366118314b978f94b64c8636
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032813"
---
# <a name="didiskquotauser-object"></a>DiDiskQuotaUser, objeto

Permite a un cliente administrar la configuración de cuota global de disco de un volumen NTFS. Este objeto hace que la funcionalidad esencial de la **interfaz DIDiskQuotaUser** esté disponible para scripting y aplicaciones basadas Visual Basic Microsoft.

## <a name="members"></a>Miembros

El **objeto DIDiskQuotaUser** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto DIDiskQuotaUser** tiene estos métodos.



| Método                                           | Descripción                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [**Invalidate**](didiskquotauser-invalidate.md) | Borra la información de usuario almacenada en caché del objeto.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto DIDiskQuotaUser** tiene estas propiedades.



| Propiedad                                                                        | Tipo de acceso           | Descripción                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**AccountContainerName**](didiskquotauser-accountcontainername.md)<br/> | Solo lectura<br/>  | Obtiene el nombre del contenedor de cuentas del usuario.<br/>                                            |
| [**AccountStatus**](didiskquotauser-accountstatus.md)<br/>               | Solo lectura<br/>  | Obtiene el estado de la cuenta del usuario.<br/>                                                    |
| [**Displayname**](didiskquotauser-displayname.md)<br/>                   | Solo lectura<br/>  | Obtiene el nombre para mostrar del usuario.<br/>                                                             |
| [**ID**](didiskquotauser-id.md)<br/>                                     | Solo lectura<br/>  | Obtiene un identificador que identifica de forma única al usuario.<br/>                                             |
| [**LogonName**](didiskquotauser-logonname.md)<br/>                       | Solo lectura<br/>  | Obtiene el nombre de la cuenta de inicio de sesión del usuario.<br/>                                                       |
| [**QuotaLimit**](didiskquotauser-quotalimit.md)<br/>                     | Lectura/escritura<br/> | Establece u obtiene el límite de cuota actual [**del usuario.**](diskquotacontrol-object.md)<br/>           |
| [**QuotaLimitText**](didiskquotauser-quotalimittext.md)<br/>             | Solo lectura<br/>  | Obtiene el límite de cuota actual [**del usuario**](diskquotacontrol-object.md) como una cadena de texto. <br/> |
| [**QuotaThreshold**](didiskquotauser-quotathreshold.md)<br/>             | Lectura/escritura<br/> | Establece u obtiene el umbral de advertencia del usuario, en bytes.<br/>                                      |
| [**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)<br/>     | Solo lectura<br/>  | Obtiene el umbral de advertencia del usuario como una cadena de texto.<br/>                                       |
| [**QuotaUsed**](didiskquotauser-quotaused.md)<br/>                       | Solo lectura<br/>  | Obtiene el uso actual del disco del usuario, en bytes.<br/>                                             |
| [**QuotaUsedText**](didiskquotauser-quotausedtext.md)<br/>               | Solo lectura<br/>  | Obtiene el uso actual del disco del usuario como una cadena de texto.<br/>                                      |



 

## <a name="remarks"></a>Comentarios

Cada usuario del volumen administrado por el objeto [**DiskQuotaControl**](diskquotacontrol-object.md) tiene asociado un objeto **DIDiskQuotaUser.** Este objeto permite a un cliente administrar la configuración de un usuario individual. Hay varias maneras de obtener el objeto **DIDiskQuotaUser de** un usuario:

-   Los **objetos DIDiskQuotaUser** para todos los usuarios con cuotas en el volumen se exponen como una colección y se pueden enumerar. A continuación se describe cómo enumerar **objetos DIDiskQuotaUser.**
-   Al agregar un nuevo usuario, el [**método AddUser**](diskquotacontrol-adduser.md) devuelve el objeto **DIDiskQuotaUser del** usuario.
-   Si tiene el nombre del usuario, el [**método FindUser**](diskquotacontrol-finduser.md) devuelve el objeto **DIDiskQuotaUser del** usuario.

### <a name="enumerating-disk-quota-users"></a>Enumeración de usuarios de cuota de disco

Los **objetos DIDiskQuotaUser** para todos los usuarios con una cuota en el volumen se exponen como una colección. El [**objeto DiskQuotaControl**](diskquotacontrol-object.md) exporta un método de enumerador estándar que permite enumerar la colección de objetos **DIDiskQuotaUser.** El procedimiento siguiente muestra cómo realizar la enumeración con Microsoft JScript (compatible con la especificación del lenguaje ECMA 262). Puede usar un procedimiento similar con Visual Basic o Microsoft Visual Basic Scripting Edition (VBScript).

1.  Cree un nuevo [**objeto DiskQuotaControl.**](diskquotacontrol-object.md)
2.  Inicialíctelo [**con Inicializar**](diskquotacontrol-initialize.md).
3.  Cree un nuevo JScript **objeto Enumerador.**
4.  Use un **bucle for** para enumerar los **objetos DIDiskQuotaUser.** No es necesario establecer un valor inicial. El método **moveNext** del objeto enumerador notifica al método **item** que devuelva el siguiente **objeto DIDiskQuotaUser.** El **método atEnd** devuelve **false** cuando se llega al final de la lista.
5.  Según sea necesario, use el objeto **DIDiskQuotaUser** devuelto por el método **item** del enumerador para recuperar o establecer una o varias de las propiedades de cuota de disco del usuario asociado.

En el fragmento de código siguiente se muestra cómo enumerar **objetos DIDiskQuotaUser** con JScript. El **argumento \_ Volume Label** que se pasa a la función **EnumUsers** es un valor de cadena que contiene una etiqueta de volumen como "C: \\ \\ ".


```
function EnumUsers(Volume_Label)
{
    var Volume;
    var QuotaUsers;
    var QuotaUser;

    Volume = new ActiveXObject("Microsoft.DiskQuota.1");
    Volume.Initialize(Volume_Label, 1);

    QuotaUsers = new Enumerator(Volume);
    for (;!Users.atEnd(); Users.moveNext())
    {
       QuotaUser = QuotaUsers.item();

     //Use the QuotaUser object to retrieve or set one or more
     //of the user's disk quota properties
     ...
    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                                    |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                          |
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5.0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto shell**](shell.md)
</dt> </dl>

 

 




