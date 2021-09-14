---
description: Abre un almacén de certificados especificado.
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Método Store.Open
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170854"
---
# <a name="storeopen-method"></a>Método Store.Open

\[El **método Open** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. En su lugar, use [**la clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

El **método Open** abre un almacén de certificados [*especificado.*](../secgloss/c-gly.md) De forma predeterminada, la ubicación DEL ALMACÉN DE USUARIOS ACTUAL DE CAPICOM y EL ALMACÉN DE MI TIENDA DE \_ \_ \_ CAPICOM \_ \_ se abren como de solo lectura.

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

Valor de la [enumeración CAPICOM \_ STORE \_ LOCATION](capicom-store-location.md) que indica la ubicación del almacén que se va a abrir. El valor predeterminado es CAPICOM \_ CURRENT \_ USER \_ STORE. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                              | Significado                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**ALMACÉN DE USUARIOS DE CAPICOM \_ ACTIVE \_ DIRECTORY \_ \_**</dt> </dl> | El almacén es un Active Directory almacén. No se generará ningún error si un Active Directory se abre como lectura/escritura, pero los cambios en el almacén no se conservarán. Los certificados no se pueden agregar ni quitar de Active Directory almacenes.<br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**ALMACÉN DE USUARIOS \_ ACTUAL DE CAPICOM \_ \_**</dt> </dl>                             | El almacén es un almacén de usuario actual. Un almacén de usuario actual puede ser un almacén de lectura y escritura. Si es así, se conservan los cambios en el contenido del almacén.<br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**CAPICOM \_ LOCAL \_ MACHINE \_ STORE**</dt> </dl>                          | El almacén es un almacén de equipos local. Los almacenes de equipos locales solo pueden ser almacenes de lectura y escritura si el usuario tiene permisos de lectura y escritura. Si el usuario tiene permisos de lectura y escritura y si el almacén se abre de lectura y escritura, los cambios en el contenido del almacén se conservan.<br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**ALMACÉN DE MEMORIA \_ CAPICOM \_**</dt> </dl>                                                | El almacén es un almacén de memoria. Los cambios en el contenido del almacén no se conservan.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**ALMACÉN DE USUARIOS \_ DE \_ TARJETA INTELIGENTE CAPICOM \_ \_**</dt> </dl>                   | La tienda es el grupo de tarjetas inteligentes presentes. Introducido en CAPICOM 2.0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*StoreName* \[ en, opcional\]
</dt> <dd>

Cadena que contiene el nombre del almacén de certificados del sistema que se va a abrir. El valor predeterminado es CAPICOM \_ MY \_ STORE. Si el almacén se abre desde un script web, no se permite el carácter de barra diagonal inversa ( \\ ) en el nombre. Además de los almacenes definidos por el sistema, se pueden abrir almacenes definidos por el usuario.

Este parámetro puede ser un almacén definido por el usuario o uno de los siguientes almacenes de certificados del sistema.



| Value                                                                                                                                                                            | Significado                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <dt>**CAPICOM \_ CA \_ STORE**</dt> </dl>          | Almacén de CA. Este almacén se usa para almacenar certificados de entidad de certificación intermedios.<br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <dt>**CAPICOM \_ MY \_ STORE**</dt> </dl>          | Mi tienda. Este almacén se usa para los certificados personales de un usuario.<br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <dt>**CAPICOM \_ OTHER \_ STORE**</dt> </dl> | Almacén de libretas de direcciones. Este almacén se usa para mantener los certificados de otros usuarios.<br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <dt>**ALMACÉN RAÍZ \_ CAPICOM \_**</dt> </dl>    | Almacén raíz. Este almacén se usa para almacenar la entidad de certificación raíz y los certificados autofirmados y de confianza.<br/> |



 

</dd> <dt>

*OpenMode* \[ en, opcional\]
</dt> <dd>

Valor de la [enumeración CAPICOM \_ STORE OPEN \_ \_ MODE](capicom-store-open-mode.md) que indica el modo abierto del almacén. El valor predeterminado es CAPICOM \_ STORE \_ OPEN READ \_ \_ ONLY. Si el almacén se abre desde un script web, este valor se fuerza a CAPICOM \_ STORE \_ OPEN EXISTING \_ \_ ONLY. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                           | Significado                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <dt>**MÁXIMO PERMITIDO DE \_ APERTURA \_ DE LA TIENDA \_ CAPICOM \_**</dt> </dl> | Abra el almacén en modo de lectura y escritura si el usuario tiene permisos de lectura y escritura. De lo contrario, abra el almacén en modo de solo lectura.<br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ READ \_ ONLY**</dt> </dl>                   | Abra el almacén en modo de solo lectura.<br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ READ \_ WRITE**</dt> </dl>                | Abra el almacén en modo de lectura y escritura.<br/>                                                                                     |



 

Las marcas siguientes se pueden combinar con los valores de la tabla anterior mediante una operación **OR** lógica.



| Value                                                                                                                                                                                                                              | Significado                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ EXISTING \_ ONLY**</dt> </dl>          | Abrir solo almacenes existentes; no cree un nuevo almacén. Introducido en CAPICOM 2.0.<br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ INCLUDE \_ ARCHIVED**</dt> </dl> | Incluir certificados archivados al usar el almacén. Introducido en CAPICOM 2.0.<br/>   |



 

Las tiendas de algunas ubicaciones solo se pueden abrir en modo de solo lectura. Estos incluyen todos los almacenes de CAPICOM LOCAL MACHINE STORE para los que el \_ usuario no tiene permisos de \_ \_ escritura. Los intentos de abrir un almacén como un almacén de lectura y escritura sin el acceso y los permisos adecuados provocarán el error del **método Open.** Active Directory se pueden abrir como un almacén de lectura y escritura sin errores del método **Open,** pero los cambios en el almacén no se conservarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si se llama a este método en un almacén de Tarjeta inteligente, se pueden invocar interfaces de usuario de SmartCard adicionales.

> [!IMPORTANT]
> Cuando se llama a este método desde un script web, el script debe tener acceso a los certificados digitales en el equipo local. Si permite que el script acceda a los certificados digitales, el sitio web desde el que se ejecuta el script también obtendrá acceso a cualquier información personal almacenada en los certificados. La primera vez que se llama a este método desde un dominio determinado, se genera un cuadro de diálogo en el que el usuario debe indicar si se debe permitir el acceso a los certificados. Los almacenes abiertos desde un script web fuerzan automáticamente la marca CAPICOM \_ STORE \_ OPEN EXISTING \_ \_ ONLY.

 

Si *StoreLocation es* **CAPICOM \_ SMART CARD USER \_ \_ \_ STORE,** *StoreName* se omite. En este caso, CAPICOM lee todos los certificados de todos los lectores disponibles que contienen una tarjeta inteligente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|----------------------------------------------------------------------------------------|
| Redistribuible<br/> | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tienda**](store.md)
</dt> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> <dt>

[**Cerca**](store-close.md)
</dt> </dl>

 

 
