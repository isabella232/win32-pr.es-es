---
description: Abre un almacén de certificados especificado.
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Store. Open (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: ef4ffe89a4b726ecfa33fb95d213d809cae2487b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670712"
---
# <a name="storeopen-method"></a>Store. Open (método)

\[El método **Open** está disponible para su uso en los sistemas operativos especificados en la sección requirements. En su lugar, use la [**clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

El método **Open** abre un [*almacén de certificados*](../secgloss/c-gly.md)especificado. De forma predeterminada, la \_ Ubicación del almacén de usuarios actual de CAPICOM \_ \_ y CAPICOM \_ My \_ Store Store se abren como de solo lectura.

## <a name="syntax"></a>Sintaxis


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StoreLocation* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de [ \_ \_ Ubicación del almacén de CAPICOM](capicom-store-location.md) que indica la ubicación del almacén que se va a abrir. El valor predeterminado es el \_ almacén del usuario actual de CAPICOM \_ \_ . Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**el \_ \_ almacén de \_ usuarios de Active \_ Directory de CAPICOM**</dt> </dl> | El almacén es un almacén de Active Directory. No se generará ningún error si se abre un almacén de Active Directory como de lectura/escritura, pero no se conservarán los cambios realizados en el almacén. Los certificados no se pueden agregar ni quitar de Active Directory almacenes.<br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**\_almacén de \_ usuarios \_ actual de CAPICOM**</dt> </dl>                             | El almacén es un almacén de usuario actual. Un almacén de usuario actual puede ser un almacén de lectura/escritura. Si es así, se conservan los cambios en el contenido del almacén.<br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**\_almacén del \_ equipo \_ local de CAPICOM**</dt> </dl>                          | El almacén es un almacén del equipo local. Los almacenes de equipos locales pueden ser almacenes de lectura/escritura solo si el usuario tiene permisos de lectura y escritura. Si el usuario tiene permisos de lectura y escritura y si el almacén está abierto para lectura y escritura, se conservan los cambios en el contenido del almacén.<br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**\_almacén de memoria CAPICOM \_**</dt> </dl>                                                | El almacén es un almacén de memoria. No se conservan los cambios en el contenido del almacén.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**el \_ \_ almacén de \_ usuarios de tarjetas inteligentes CAPICOM \_**</dt> </dl>                   | El almacén es el grupo de tarjetas inteligentes presentes. Introducido en CAPICOM 2,0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*StoreName* \[ en, opcional\]
</dt> <dd>

Cadena que contiene el nombre del almacén de certificados del sistema que se va a abrir. El valor predeterminado es CAPICOM \_ My \_ Store. Si el almacén se abre desde un script Web, \\ no se permite el carácter de barra diagonal inversa () en el nombre. Además de los almacenes definidos por el sistema, se pueden abrir los almacenes definidos por el usuario.

Este parámetro puede ser un almacén definido por el usuario o uno de los siguientes almacenes de certificados del sistema.



| Value                                                                                                                                                                            | Significado                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <dt>**\_almacén de CA de CAPICOM \_**</dt> </dl>          | Almacén de CA. Este almacén se usa para almacenar certificados de entidad de certificación intermedios.<br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <dt>**CAPICOM \_ My \_ Store**</dt> </dl>          | Mi tienda. Este almacén se utiliza para los certificados personales de un usuario.<br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <dt>**\_otra \_ tienda de CAPICOM**</dt> </dl> | Tienda de la AddressBook. Este almacén se utiliza para mantener los certificados de otros usuarios.<br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <dt>**\_almacén raíz de CAPICOM \_**</dt> </dl>    | Almacén raíz. Este almacén se usa para almacenar la CA raíz y los certificados de confianza autofirmados.<br/> |



 

</dd> <dt>

*OpenMode* \[ en, opcional\]
</dt> <dd>

Un valor de la enumeración de modo de apertura de la [ \_ tienda \_ \_ CAPICOM](capicom-store-open-mode.md) que indica el modo de apertura del almacén. El valor predeterminado es CAPICOM \_ Store \_ Open \_ Read \_ only. Si el almacén se abre desde un script Web, este valor se fuerza a que \_ CAPICOM \_ solo esté abierto \_ \_ . Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                           | Significado                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <dt>**\_ \_ \_ máximo permitido del almacén \_ de CAPICOM**</dt> </dl> | Abra el almacén en modo de lectura y escritura si el usuario tiene permisos de lectura/escritura; de lo contrario, abra el almacén en modo de solo lectura.<br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <dt>**CAPICOM \_ Store \_ Open \_ Read \_ Only**</dt> </dl>                   | Abra el almacén en modo de solo lectura.<br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <dt>**CAPICOM \_ Store \_ Open \_ Read \_ Write**</dt> </dl>                | Abra el almacén en modo de lectura y escritura.<br/>                                                                                     |



 

Las marcas siguientes se pueden combinar con los valores de la tabla anterior mediante una operación **or** lógica.



| Value                                                                                                                                                                                                                              | Significado                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <dt>**CAPICOM \_ Store \_ Open \_ exist \_ Only**</dt> </dl>          | Abrir solo los almacenes existentes; no cree un nuevo almacén. Introducido en CAPICOM 2,0.<br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <dt>**\_ \_ archivos abiertos de \_ la tienda de CAPICOM \_**</dt> </dl> | Incluir certificados archivados al usar el almacén. Introducido en CAPICOM 2,0.<br/>   |



 

Los almacenes en algunas ubicaciones solo se pueden abrir en modo de solo lectura. Estos incluyen todas las tiendas del \_ \_ almacén de la máquina local CAPICOM para las \_ que el usuario no tiene permisos de escritura. Si intenta abrir un almacén como un almacén de lectura/escritura sin el acceso y los permisos adecuados, se producirá un error en el método **Open** . Active Directory almacenes se pueden abrir como un almacén de lectura/escritura sin errores en el método **abierto** , pero no se conservarán los cambios en el almacén.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si se llama a este método en un almacén de tarjetas inteligentes, se pueden invocar interfaces de usuario de tarjeta inteligente adicionales.

> [!IMPORTANT]
> Cuando se llama a este método desde un script Web, el script debe tener acceso a los certificados digitales en el equipo local. Si permite que el script tenga acceso a los certificados digitales, el sitio web desde el que se ejecuta el script también obtendrá acceso a cualquier información personal almacenada en los certificados. La primera vez que se llama a este método desde un dominio determinado, se genera un cuadro de diálogo en el que el usuario debe indicar si se debe permitir el acceso a los certificados. Los almacenes abiertos desde un script web obligan automáticamente a la \_ \_ marca CAPICOM Open \_ exist \_ only.

 

Si *StoreLocation* es **el \_ \_ almacén de \_ usuarios \_ de tarjetas inteligentes CAPICOM**, *StoreName* se omite. En este caso, CAPICOM Lee todos los certificados de todos los lectores disponibles que contienen una tarjeta inteligente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Store**](store.md)
</dt> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**Cercanos**](store-close.md)
</dt> </dl>

 

 
