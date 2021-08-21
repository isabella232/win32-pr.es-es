---
title: Restaurar objetos eliminados
description: Windows Server 2003 incluye \ 0034;restaurar objetos eliminados \ 0034; Característica.
ms.assetid: b64c5c91-fb76-4323-b78d-f692aa887c96
ms.tgt_platform: multiple
keywords:
- Restauración de objetos eliminados de AD
- Active Directory, mediante, restaurar objetos eliminados
- objetos ad , restaurar objetos eliminados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 431bcddcbd15366a6accf9b8368fa8d34377b27af923fb102803b6316462634e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025123"
---
# <a name="restoring-deleted-objects"></a>Restaurar objetos eliminados

Windows Server 2003 incluye la característica "restaurar objetos eliminados".

Para habilitar la restauración de objetos eliminados, al menos un controlador de dominio del dominio debe ejecutarse en Windows Server 2003 o en una versión posterior de Windows. De forma predeterminada, solo los administradores de dominio pueden restaurar objetos eliminados, aunque esto se puede delegar a otros.

Las siguientes limitaciones se aplican a la restauración de objetos eliminados:

-   No se puede restaurar un objeto cuando la duración del objeto ha expirado porque, cuando ha expirado la duración del mismo, el objeto se elimina permanentemente.
-   Los objetos que existen en la raíz del contexto de nomenclatura, como un dominio o una partición de aplicación, no se pueden restaurar.
-   Los objetos de esquema no se pueden restaurar. Los objetos de esquema nunca se deben eliminar.
-   Es posible restaurar los contenedores eliminados, pero la restauración de los objetos eliminados que estaban en el contenedor antes de la eliminación es difícil porque la estructura de árbol bajo el contenedor debe reconstruirse manualmente.

## <a name="permissions-required-to-restore-a-deleted-object"></a>Permisos necesarios para restaurar un objeto eliminado

Cuando se elimina un objeto, se conserva el descriptor de seguridad del objeto. Aunque el propietario se puede identificar desde el descriptor de seguridad, por motivos de seguridad, solo los administradores de dominio pueden restaurar objetos eliminados. Los administradores de dominio pueden conceder el permiso para restaurar objetos de eliminación a otros usuarios y grupos concediendo al usuario o grupo el derecho de acceso de control "Reanimate Tombstone". El derecho de acceso de control "Reanimate Tombstone" se concede en la raíz contexto de nomenclatura. Solo los usuarios que tenían permiso de acceso de lectura en un objeto y sus atributos pueden leer el objeto y los atributos accesibles después de eliminar el objeto.

> [!Note]  
> Conceder este permiso a un usuario puede ser un riesgo de seguridad porque podría permitir al usuario restaurar un objeto de cuenta que tenga acceso a recursos a los que normalmente no tendría acceso el usuario. Al restaurar una cuenta, el usuario obtiene básicamente el control de esta cuenta porque el usuario debe establecer la contraseña inicial en la cuenta cuando se restaura la cuenta.

 

Para restaurar completamente un objeto eliminado, el usuario debe:

-   Tener o ser miembro de un grupo que tenga el derecho de acceso de control "Reanimate Tombstone".

-   Tener acceso de escritura para cada atributo obligatorio que requiera actualización.

-   Tener acceso de escritura al nombre distintivo relativo (RDN).

-   Tener acceso de escritura a cada atributo opcional que deba actualizarse.

-   Tener derechos de creación de elementos secundarios en el contenedor de destino para la clase de objeto del objeto restaurado.

    > [!Note]  
    > El **atributo isDeleted** no se comprueba durante la operación de restauración. Tampoco se comprobará el permiso delete-child en el contenedor "Deleted Objects".

     

## <a name="restoring-a-deleted-object"></a>Restaurar un objeto eliminado

Para restaurar un objeto eliminado, el objeto debe encontrarse primero en el contenedor Objetos eliminados. Para obtener más información sobre cómo recuperar objetos eliminados, vea [Recuperar objetos eliminados.](retrieving-deleted-objects.md)

Cuando se ha ubicado el objeto , las siguientes operaciones deben completarse en una única operación LDAP. Esto requiere el uso de la función [**ldap \_ modify ext \_ \_ s**](/previous-versions/windows/desktop/api/winldap/nf-winldap-ldap_modify_ext_s) con el control [**\_ \_ \_ \_ OID SHOW DELETED de LDAP SERVER.**](/previous-versions/windows/desktop/ldap/ldap-server-show-deleted-oid)

-   Quite el **valor del atributo isDeleted.** El **valor del atributo isDeleted** debe quitarse, no establecerse en **FALSE.**
-   Reemplace el nombre distintivo del objeto para que se traslade a un contenedor que no sea el contenedor Objetos eliminados. Puede ser cualquier contenedor que normalmente pueda contener el objeto . El nombre distintivo del contenedor anterior del objeto se puede encontrar en el atributo **lastKnownParent** del objeto eliminado. El **atributo lastKnownParent** solo se establece si el objeto se eliminó en un Windows de dominio de Server 2003. Por lo tanto, es posible que el contenido del atributo **lastKnownParent** sea inexacto.
-   Restaure los atributos obligatorios para el objeto que se borraron durante la eliminación.

> [!Note]  
> El **atributo objectCategory** también se puede establecer cuando se restaura el objeto, pero no es necesario. Si no se especifica ningún valor **objectCategory,** se usa **el valor predeterminado objectCategory** para **objectClass** del objeto.

 

Una vez restaurado el objeto, se puede acceder a él tal y como estaba antes de que se eliminara. En este momento, se deben restaurar los atributos opcionales que sean importantes. También se deben restaurar las referencias al objeto desde otros objetos del directorio.

Como medida de seguridad, los objetos de usuario se deshabilitan cuando se restauran. Los objetos de usuario deben habilitarse después de restaurar los atributos opcionales para permitir el uso del objeto de usuario.

Para obtener más información y un ejemplo de código que muestra cómo restaurar un objeto eliminado, vea la función RestoreDeletedObject a continuación.

## <a name="restoredeletedobject"></a>RestoreDeletedObject

En el siguiente ejemplo de código de C++ se muestra cómo restaurar un objeto eliminado.


```C++
//***************************************************************************
//
//  RestoreDeletedObject()
//
//  Restores a deleted object. 
//
//  pwszDeletedDN - Contains the fully qualified distinguished name of the 
//  deleted object.
//
//  pwszDestContainerDN - Contains the fully qualified distinguished name of 
//  the folder that the deleted object should be moved to.
//
//  Returns S_OK if successful or an HRESULT or LDAP error code otherwise.
//
//***************************************************************************

HRESULT RestoreDeletedObject(LPCWSTR pwszDeletedDN, LPCWSTR pwszDestContainerDN)
{
    if((NULL == pwszDeletedDN) || (NULL == pwszDestContainerDN))
    {
        return E_POINTER;
    }
    
    HRESULT hr = E_FAIL;

    // Build the new distinguished name.
    LPWSTR pwszNewDN = new WCHAR[lstrlenW(pwszDeletedDN) + lstrlenW(pwszDestContainerDN) + 1];
    if(pwszNewDN)
    {
        wcscpy_s(pwszNewDN, pwszDeletedDN);

        // Search for the first 0x0A character. This is the delimiter in the deleted object name.
        LPWSTR pwszChar;
        for(pwszChar = pwszNewDN; *pwszChar; pwszChar = CharNextW(pwszChar))
        {
            if(('\\' == *pwszChar) && ('0' == *(pwszChar + 1)) && ('A' == *(pwszChar + 2)))
            {
                break;
            }
            
        }

        if(0 != *pwszChar)
        {
            // Truncate the name string at the delimiter.
            *pwszChar = 0;

            // Add the last known parent DN to complete the DN.
            wcscat_s(pwszNewDN, L",");
            wcscat_s(pwszNewDN, pwszDestContainerDN);

            PLDAP ld;

            // Initialize LDAP.
            ld = ldap_init(NULL, LDAP_PORT);
            if(NULL != ld) 
            {
                ULONG ulRC;
                ULONG version = LDAP_VERSION3;

                // Set the LDAP version.
                ulRC = ldap_set_option(ld, LDAP_OPT_PROTOCOL_VERSION, (void*)&version);
                if(LDAP_SUCCESS == ulRC)
                {
                    // Establish a connection with the server.
                    ulRC = ldap_connect(ld, NULL);
                    if(LDAP_SUCCESS == ulRC)
                    {                    
                        // Bind to the LDAP server.
                        ulRC = ldap_bind_s(ld, NULL, NULL, LDAP_AUTH_NEGOTIATE);
                        if(LDAP_SUCCESS == ulRC)
                        {
                            // Setup the new values.
                            LPWSTR rgNewVals[] = {pwszNewDN, NULL};

                            /*
                            Remove the isDeleted attribute. This cannot be set 
                            to FALSE or the restore operation will not work.
                            */
                            LDAPModW modIsDeleted = { LDAP_MOD_DELETE, L"isDeleted", NULL };

                            /*
                            Set the new DN, in effect, moving the deleted 
                            object to where it resided before the deletion.
                            */
                            LDAPModW modDN = { LDAP_MOD_REPLACE, L"distinguishedName", rgNewVals };
                            
                            // Initialize the LDAPMod structure.
                            PLDAPModW ldapMods[] = 
                            {
                                &modIsDeleted,
                                &modDN,
                                NULL
                            };

                            /*
                            Use the LDAP_SERVER_SHOW_DELETED_OID control to 
                            modify deleted objects.
                            */
                            LDAPControlW showDeletedControl;
                            showDeletedControl.ldctl_oid = LDAP_SERVER_SHOW_DELETED_OID_W;
                            showDeletedControl.ldctl_value.bv_len = 0;
                            showDeletedControl.ldctl_value.bv_val = NULL;
                            showDeletedControl.ldctl_iscritical = TRUE;

                            // Initialzie the LDAPControl structure
                            PLDAPControlW ldapControls[] = { &showDeletedControl, NULL };

                            /*
                            Modify the specified attributes. This must performed 
                            in one step, which is why the LDAP APIs must be used 
                            to restore a deleted object.
                            */
                            ulRC = ldap_modify_ext_sW(ld, (PWCHAR)pwszDeletedDN, ldapMods, ldapControls, NULL);
                            if(LDAP_SUCCESS == ulRC)
                            {
                                hr = S_OK;
                            }
                            else if(LDAP_ALREADY_EXISTS == ulRC)
                            {
                                /*
                                An object already exists with the specified name 
                                in the specified target container. At this point, 
                                a new name must be selected.
                                */
                            }
                        }
                    }
                }

                if(LDAP_SUCCESS != ulRC)
                {
                    hr = ulRC;
                    
                    OutputDebugString(ldap_err2string(ulRC));
                }

                // Release the LDAP session.
                ldap_unbind(ld);
            }
        }
        else
        {
            /*
            If the end of the string is reached before the delimiter is found, just 
            end and fail.
            */
            hr = E_INVALIDARG;
        }
    
        delete pwszNewDN;
    }
    else
    {
        hr = E_OUTOFMEMORY;
    }

    return hr;
}

```



 

 