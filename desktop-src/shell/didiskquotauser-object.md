---
description: Permite a un cliente administrar la configuración de cuota de disco global de un volumen NTFS. Este objeto hace que la funcionalidad esencial de la interfaz DIDiskQuotaUser esté disponible para las aplicaciones de scripting y basadas en Microsoft Visual Basic.
title: Objeto DIDiskQuotaUser
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
ms.openlocfilehash: 5699ad9d15b0fa31c92f7d88df194f9012fa679d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104984275"
---
# <a name="didiskquotauser-object"></a>Objeto DIDiskQuotaUser

Permite a un cliente administrar la configuración de cuota de disco global de un volumen NTFS. Este objeto hace que la funcionalidad esencial de la interfaz **DIDiskQuotaUser** esté disponible para las aplicaciones de scripting y basadas en Microsoft Visual Basic.

## <a name="members"></a>Miembros

El objeto **DIDiskQuotaUser** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **DIDiskQuotaUser** tiene estos métodos.



| Método                                           | Descripción                                             |
|:-------------------------------------------------|:--------------------------------------------------------|
| [**Invalidar**](didiskquotauser-invalidate.md) | Borra la información de usuario almacenada en caché del objeto.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **DIDiskQuotaUser** tiene estas propiedades.



| Propiedad                                                                        | Tipo de acceso           | Descripción                                                                                          |
|:--------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------|
| [**AccountContainerName**](didiskquotauser-accountcontainername.md)<br/> | Solo lectura<br/>  | Obtiene el nombre del contenedor de cuentas del usuario.<br/>                                            |
| [**Estados**](didiskquotauser-accountstatus.md)<br/>               | Solo lectura<br/>  | Obtiene el estado de la cuenta del usuario.<br/>                                                    |
| [**DisplayName**](didiskquotauser-displayname.md)<br/>                   | Solo lectura<br/>  | Obtiene el nombre para mostrar del usuario.<br/>                                                             |
| [**ID**](didiskquotauser-id.md)<br/>                                     | Solo lectura<br/>  | Obtiene un identificador que identifica de forma única al usuario.<br/>                                             |
| [**LogonName**](didiskquotauser-logonname.md)<br/>                       | Solo lectura<br/>  | Obtiene el nombre de la cuenta de inicio de sesión del usuario.<br/>                                                       |
| [**QuotaLimit**](didiskquotauser-quotalimit.md)<br/>                     | Lectura/escritura<br/> | Establece u obtiene el [**límite de cuota**](diskquotacontrol-object.md)actual del usuario.<br/>           |
| [**QuotaLimitText**](didiskquotauser-quotalimittext.md)<br/>             | Solo lectura<br/>  | Obtiene el [**límite de cuota**](diskquotacontrol-object.md) actual del usuario como una cadena de texto. <br/> |
| [**QuotaThreshold**](didiskquotauser-quotathreshold.md)<br/>             | Lectura/escritura<br/> | Establece u obtiene el umbral de advertencia del usuario, en bytes.<br/>                                      |
| [**QuotaThresholdText**](didiskquotauser-quotathresholdtext.md)<br/>     | Solo lectura<br/>  | Obtiene el umbral de advertencia del usuario como una cadena de texto.<br/>                                       |
| [**QuotaUsed**](didiskquotauser-quotaused.md)<br/>                       | Solo lectura<br/>  | Obtiene el uso actual del disco del usuario, en bytes.<br/>                                             |
| [**QuotaUsedText**](didiskquotauser-quotausedtext.md)<br/>               | Solo lectura<br/>  | Obtiene el uso actual del disco del usuario como una cadena de texto.<br/>                                      |



 

## <a name="remarks"></a>Observaciones

Cada usuario del volumen administrado por el objeto [**DiskQuotaControl**](diskquotacontrol-object.md) tiene un objeto **DIDiskQuotaUser** asociado a él. Este objeto permite a un cliente administrar la configuración de un usuario individual. Hay varias maneras de obtener el objeto **DIDiskQuotaUser** de un usuario:

-   Los objetos **DIDiskQuotaUser** para todos los usuarios con cuotas en el volumen se exponen como una colección y se pueden enumerar. A continuación se explica cómo enumerar los objetos **DIDiskQuotaUser** .
-   Al agregar un nuevo usuario, el método [**adduser**](diskquotacontrol-adduser.md) devuelve el objeto **DIDiskQuotaUser** del usuario.
-   Si tiene el nombre del usuario, el método [**FindUser**](diskquotacontrol-finduser.md) devuelve el objeto **DIDiskQuotaUser** del usuario.

### <a name="enumerating-disk-quota-users"></a>Enumerar usuarios de cuota de disco

Los objetos **DIDiskQuotaUser** para todos los usuarios con una cuota en el volumen se exponen como una colección. El objeto [**DiskQuotaControl**](diskquotacontrol-object.md) exporta un método de enumerador estándar que le permite enumerar la colección de objetos **DIDiskQuotaUser** . En el procedimiento siguiente se muestra cómo realizar la enumeración con Microsoft JScript (compatible con la especificación del lenguaje ECMA 262). Puede usar un procedimiento similar con Visual Basic o Microsoft Visual Basic Scripting Edition (VBScript).

1.  Cree un nuevo objeto [**DiskQuotaControl**](diskquotacontrol-object.md) .
2.  Inicialícelo con [**Initialize**](diskquotacontrol-initialize.md).
3.  Cree un nuevo objeto de **enumerador** de JScript.
4.  Use un bucle **for** para enumerar los objetos **DIDiskQuotaUser** . No es necesario establecer un valor inicial. El método **MoveNext** del objeto de enumerador notifica al método **Item** que debe devolver el siguiente objeto **DIDiskQuotaUser** . El método **Atend (** devuelve **false** cuando se alcanza el final de la lista.
5.  Según sea necesario, use el objeto **DIDiskQuotaUser** devuelto por el método **Item** del enumerador para recuperar o establecer una o varias propiedades de cuota de disco del usuario asociado.

En el fragmento de código siguiente se muestra cómo enumerar objetos **DIDiskQuotaUser** con JScript. El argumento de la **\_ etiqueta de volumen** que se pasa a la función **EnumUsers** es un valor de cadena que contiene una etiqueta de volumen como "C: \\ \\ ".


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
| Archivo DLL<br/>                      | <dl> <dt>Shell32.dll (versión 5,0 o posterior)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objeto de Shell**](shell.md)
</dt> </dl>

 

 




