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
# <a name="storeopen-method"></a><span data-ttu-id="667c4-103">Store. Open (método)</span><span class="sxs-lookup"><span data-stu-id="667c4-103">Store.Open method</span></span>

<span data-ttu-id="667c4-104">\[El método **Open** está disponible para su uso en los sistemas operativos especificados en la sección requirements.</span><span class="sxs-lookup"><span data-stu-id="667c4-104">\[The **Open** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="667c4-105">En su lugar, use la [**clase X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) en el espacio de nombres [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]</span><span class="sxs-lookup"><span data-stu-id="667c4-105">Instead, use the [**X509Store Class**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) namespace.\]</span></span>

<span data-ttu-id="667c4-106">El método **Open** abre un [*almacén de certificados*](../secgloss/c-gly.md)especificado.</span><span class="sxs-lookup"><span data-stu-id="667c4-106">The **Open** method opens a specified [*certificate store*](../secgloss/c-gly.md).</span></span> <span data-ttu-id="667c4-107">De forma predeterminada, la \_ Ubicación del almacén de usuarios actual de CAPICOM \_ \_ y CAPICOM \_ My \_ Store Store se abren como de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="667c4-107">By default, the CAPICOM\_CURRENT\_USER\_STORE location and CAPICOM\_MY\_STORE store are opened as read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="667c4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="667c4-108">Syntax</span></span>


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a><span data-ttu-id="667c4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="667c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="667c4-110">*StoreLocation* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="667c4-110">*StoreLocation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="667c4-111">Un valor de la enumeración de [ \_ \_ Ubicación del almacén de CAPICOM](capicom-store-location.md) que indica la ubicación del almacén que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="667c4-111">A value of the [CAPICOM\_STORE\_LOCATION](capicom-store-location.md) enumeration that indicates the location of the store to be opened.</span></span> <span data-ttu-id="667c4-112">El valor predeterminado es el \_ almacén del usuario actual de CAPICOM \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="667c4-112">The default value is CAPICOM\_CURRENT\_USER\_STORE.</span></span> <span data-ttu-id="667c4-113">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="667c4-113">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="667c4-114">Valor</span><span class="sxs-lookup"><span data-stu-id="667c4-114">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="667c4-115">Significado</span><span class="sxs-lookup"><span data-stu-id="667c4-115">Meaning</span></span>                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <span data-ttu-id="667c4-116"><dt>**el \_ \_ almacén de \_ usuarios de Active \_ Directory de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-116"><dt>**CAPICOM\_ACTIVE\_DIRECTORY\_USER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="667c4-117">El almacén es un almacén de Active Directory.</span><span class="sxs-lookup"><span data-stu-id="667c4-117">The store is an Active Directory store.</span></span> <span data-ttu-id="667c4-118">No se generará ningún error si se abre un almacén de Active Directory como de lectura/escritura, pero no se conservarán los cambios realizados en el almacén.</span><span class="sxs-lookup"><span data-stu-id="667c4-118">No error will be generated if an Active Directory store is opened as read/write, but any changes to the store will not be persisted.</span></span> <span data-ttu-id="667c4-119">Los certificados no se pueden agregar ni quitar de Active Directory almacenes.</span><span class="sxs-lookup"><span data-stu-id="667c4-119">Certificates cannot be added to or removed from Active Directory stores.</span></span><br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <span data-ttu-id="667c4-120"><dt>**\_almacén de \_ usuarios \_ actual de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-120"><dt>**CAPICOM\_CURRENT\_USER\_STORE**</dt></span></span> </dl>                             | <span data-ttu-id="667c4-121">El almacén es un almacén de usuario actual.</span><span class="sxs-lookup"><span data-stu-id="667c4-121">The store is a current user store.</span></span> <span data-ttu-id="667c4-122">Un almacén de usuario actual puede ser un almacén de lectura/escritura.</span><span class="sxs-lookup"><span data-stu-id="667c4-122">A current user store may be a read/write store.</span></span> <span data-ttu-id="667c4-123">Si es así, se conservan los cambios en el contenido del almacén.</span><span class="sxs-lookup"><span data-stu-id="667c4-123">If it is, changes in the contents of the store are persisted.</span></span><br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <span data-ttu-id="667c4-124"><dt>**\_almacén del \_ equipo \_ local de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-124"><dt>**CAPICOM\_LOCAL\_MACHINE\_STORE**</dt></span></span> </dl>                          | <span data-ttu-id="667c4-125">El almacén es un almacén del equipo local.</span><span class="sxs-lookup"><span data-stu-id="667c4-125">The store is a local computer store.</span></span> <span data-ttu-id="667c4-126">Los almacenes de equipos locales pueden ser almacenes de lectura/escritura solo si el usuario tiene permisos de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="667c4-126">Local computer stores can be read/write stores only if the user has read/write permissions.</span></span> <span data-ttu-id="667c4-127">Si el usuario tiene permisos de lectura y escritura y si el almacén está abierto para lectura y escritura, se conservan los cambios en el contenido del almacén.</span><span class="sxs-lookup"><span data-stu-id="667c4-127">If the user has read/write permissions and if the store is opened read/write, then changes in the contents of the store are persisted.</span></span><br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <span data-ttu-id="667c4-128"><dt>**\_almacén de memoria CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-128"><dt>**CAPICOM\_MEMORY\_STORE**</dt></span></span> </dl>                                                | <span data-ttu-id="667c4-129">El almacén es un almacén de memoria.</span><span class="sxs-lookup"><span data-stu-id="667c4-129">The store is a memory store.</span></span> <span data-ttu-id="667c4-130">No se conservan los cambios en el contenido del almacén.</span><span class="sxs-lookup"><span data-stu-id="667c4-130">Any changes in the contents of the store are not persisted.</span></span><br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <span data-ttu-id="667c4-131"><dt>**el \_ \_ almacén de \_ usuarios de tarjetas inteligentes CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-131"><dt>**CAPICOM\_SMART\_CARD\_USER\_STORE**</dt></span></span> </dl>                   | <span data-ttu-id="667c4-132">El almacén es el grupo de tarjetas inteligentes presentes.</span><span class="sxs-lookup"><span data-stu-id="667c4-132">The store is the group of present smart cards.</span></span> <span data-ttu-id="667c4-133">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="667c4-133">Introduced in CAPICOM 2.0.</span></span><br/>                                                                                                                                                                                               |



 

</dd> <dt>

<span data-ttu-id="667c4-134">*StoreName* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="667c4-134">*StoreName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="667c4-135">Cadena que contiene el nombre del almacén de certificados del sistema que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="667c4-135">A string that contains the name of the system certificate store to be opened.</span></span> <span data-ttu-id="667c4-136">El valor predeterminado es CAPICOM \_ My \_ Store.</span><span class="sxs-lookup"><span data-stu-id="667c4-136">The default value is CAPICOM\_MY\_STORE.</span></span> <span data-ttu-id="667c4-137">Si el almacén se abre desde un script Web, \\ no se permite el carácter de barra diagonal inversa () en el nombre.</span><span class="sxs-lookup"><span data-stu-id="667c4-137">If the store is opened from a web script, the backslash (\\) character is not allowed in the name.</span></span> <span data-ttu-id="667c4-138">Además de los almacenes definidos por el sistema, se pueden abrir los almacenes definidos por el usuario.</span><span class="sxs-lookup"><span data-stu-id="667c4-138">In addition to stores defined by the system, user-defined stores can be opened.</span></span>

<span data-ttu-id="667c4-139">Este parámetro puede ser un almacén definido por el usuario o uno de los siguientes almacenes de certificados del sistema.</span><span class="sxs-lookup"><span data-stu-id="667c4-139">This parameter can be a user-defined store or one of the following system certificate stores.</span></span>



| <span data-ttu-id="667c4-140">Value</span><span class="sxs-lookup"><span data-stu-id="667c4-140">Value</span></span>                                                                                                                                                                            | <span data-ttu-id="667c4-141">Significado</span><span class="sxs-lookup"><span data-stu-id="667c4-141">Meaning</span></span>                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <span data-ttu-id="667c4-142"><dt>**\_almacén de CA de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-142"><dt>**CAPICOM\_CA\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="667c4-143">Almacén de CA.</span><span class="sxs-lookup"><span data-stu-id="667c4-143">CA store.</span></span> <span data-ttu-id="667c4-144">Este almacén se usa para almacenar certificados de entidad de certificación intermedios.</span><span class="sxs-lookup"><span data-stu-id="667c4-144">This store is used to store intermediate CA certificates.</span></span><br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <span data-ttu-id="667c4-145"><dt>**CAPICOM \_ My \_ Store**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-145"><dt>**CAPICOM\_MY\_STORE**</dt></span></span> </dl>          | <span data-ttu-id="667c4-146">Mi tienda.</span><span class="sxs-lookup"><span data-stu-id="667c4-146">My store.</span></span> <span data-ttu-id="667c4-147">Este almacén se utiliza para los certificados personales de un usuario.</span><span class="sxs-lookup"><span data-stu-id="667c4-147">This store is used for a user's personal certificates.</span></span><br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <span data-ttu-id="667c4-148"><dt>**\_otra \_ tienda de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-148"><dt>**CAPICOM\_OTHER\_STORE**</dt></span></span> </dl> | <span data-ttu-id="667c4-149">Tienda de la AddressBook.</span><span class="sxs-lookup"><span data-stu-id="667c4-149">AddressBook store.</span></span> <span data-ttu-id="667c4-150">Este almacén se utiliza para mantener los certificados de otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="667c4-150">This store is used to keep the certificates of others.</span></span><br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <span data-ttu-id="667c4-151"><dt>**\_almacén raíz de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-151"><dt>**CAPICOM\_ROOT\_STORE**</dt></span></span> </dl>    | <span data-ttu-id="667c4-152">Almacén raíz.</span><span class="sxs-lookup"><span data-stu-id="667c4-152">Root store.</span></span> <span data-ttu-id="667c4-153">Este almacén se usa para almacenar la CA raíz y los certificados de confianza autofirmados.</span><span class="sxs-lookup"><span data-stu-id="667c4-153">This store is used to store the root CA and self-signed, trusted certificates.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="667c4-154">*OpenMode* \[ en, opcional\]</span><span class="sxs-lookup"><span data-stu-id="667c4-154">*OpenMode* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="667c4-155">Un valor de la enumeración de modo de apertura de la [ \_ tienda \_ \_ CAPICOM](capicom-store-open-mode.md) que indica el modo de apertura del almacén.</span><span class="sxs-lookup"><span data-stu-id="667c4-155">A value of the [CAPICOM\_STORE\_OPEN\_MODE](capicom-store-open-mode.md) enumeration that indicates the open mode of the store.</span></span> <span data-ttu-id="667c4-156">El valor predeterminado es CAPICOM \_ Store \_ Open \_ Read \_ only.</span><span class="sxs-lookup"><span data-stu-id="667c4-156">The default value is CAPICOM\_STORE\_OPEN\_READ\_ONLY.</span></span> <span data-ttu-id="667c4-157">Si el almacén se abre desde un script Web, este valor se fuerza a que \_ CAPICOM \_ solo esté abierto \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="667c4-157">If the store is opened from a web script, this value is forced to CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY.</span></span> <span data-ttu-id="667c4-158">Este parámetro puede ser uno de los valores siguientes.</span><span class="sxs-lookup"><span data-stu-id="667c4-158">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="667c4-159">Valor</span><span class="sxs-lookup"><span data-stu-id="667c4-159">Value</span></span>                                                                                                                                                                                                                           | <span data-ttu-id="667c4-160">Significado</span><span class="sxs-lookup"><span data-stu-id="667c4-160">Meaning</span></span>                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <span data-ttu-id="667c4-161"><dt>**\_ \_ \_ máximo permitido del almacén \_ de CAPICOM**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-161"><dt>**CAPICOM\_STORE\_OPEN\_MAXIMUM\_ALLOWED**</dt></span></span> </dl> | <span data-ttu-id="667c4-162">Abra el almacén en modo de lectura y escritura si el usuario tiene permisos de lectura/escritura; de lo contrario, abra el almacén en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="667c4-162">Open the store in read/write mode if the user has read/write permissions; otherwise, open the store in read-only mode.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <span data-ttu-id="667c4-163"><dt>**CAPICOM \_ Store \_ Open \_ Read \_ Only**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-163"><dt>**CAPICOM\_STORE\_OPEN\_READ\_ONLY**</dt></span></span> </dl>                   | <span data-ttu-id="667c4-164">Abra el almacén en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="667c4-164">Open the store in read-only mode.</span></span><br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <span data-ttu-id="667c4-165"><dt>**CAPICOM \_ Store \_ Open \_ Read \_ Write**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-165"><dt>**CAPICOM\_STORE\_OPEN\_READ\_WRITE**</dt></span></span> </dl>                | <span data-ttu-id="667c4-166">Abra el almacén en modo de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="667c4-166">Open the store in read/write mode.</span></span><br/>                                                                                     |



 

<span data-ttu-id="667c4-167">Las marcas siguientes se pueden combinar con los valores de la tabla anterior mediante una operación **or** lógica.</span><span class="sxs-lookup"><span data-stu-id="667c4-167">The following flags can be combined with the values in the previous table by using a logical-**OR** operation.</span></span>



| <span data-ttu-id="667c4-168">Value</span><span class="sxs-lookup"><span data-stu-id="667c4-168">Value</span></span>                                                                                                                                                                                                                              | <span data-ttu-id="667c4-169">Significado</span><span class="sxs-lookup"><span data-stu-id="667c4-169">Meaning</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <span data-ttu-id="667c4-170"><dt>**CAPICOM \_ Store \_ Open \_ exist \_ Only**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-170"><dt>**CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY**</dt></span></span> </dl>          | <span data-ttu-id="667c4-171">Abrir solo los almacenes existentes; no cree un nuevo almacén.</span><span class="sxs-lookup"><span data-stu-id="667c4-171">Open existing stores only; do not create a new store.</span></span> <span data-ttu-id="667c4-172">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="667c4-172">Introduced in CAPICOM 2.0.</span></span><br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <span data-ttu-id="667c4-173"><dt>**\_ \_ archivos abiertos de \_ la tienda de CAPICOM \_**</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-173"><dt>**CAPICOM\_STORE\_OPEN\_INCLUDE\_ARCHIVED**</dt></span></span> </dl> | <span data-ttu-id="667c4-174">Incluir certificados archivados al usar el almacén.</span><span class="sxs-lookup"><span data-stu-id="667c4-174">Include archived certificates when using the store.</span></span> <span data-ttu-id="667c4-175">Introducido en CAPICOM 2,0.</span><span class="sxs-lookup"><span data-stu-id="667c4-175">Introduced in CAPICOM 2.0.</span></span><br/>   |



 

<span data-ttu-id="667c4-176">Los almacenes en algunas ubicaciones solo se pueden abrir en modo de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="667c4-176">Stores in some locations can be opened only in read-only mode.</span></span> <span data-ttu-id="667c4-177">Estos incluyen todas las tiendas del \_ \_ almacén de la máquina local CAPICOM para las \_ que el usuario no tiene permisos de escritura.</span><span class="sxs-lookup"><span data-stu-id="667c4-177">These include all stores in CAPICOM\_LOCAL\_MACHINE\_STORE for which the user does not have write permissions.</span></span> <span data-ttu-id="667c4-178">Si intenta abrir un almacén como un almacén de lectura/escritura sin el acceso y los permisos adecuados, se producirá un error en el método **Open** .</span><span class="sxs-lookup"><span data-stu-id="667c4-178">Attempts to open a store as a read/write store without proper access and permissions will result in the failure of the **Open** method.</span></span> <span data-ttu-id="667c4-179">Active Directory almacenes se pueden abrir como un almacén de lectura/escritura sin errores en el método **abierto** , pero no se conservarán los cambios en el almacén.</span><span class="sxs-lookup"><span data-stu-id="667c4-179">Active Directory stores can be opened as a read/write store without failure of the **Open** method, but changes to the store will not be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="667c4-180">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="667c4-180">Return value</span></span>

<span data-ttu-id="667c4-181">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="667c4-181">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="667c4-182">Observaciones</span><span class="sxs-lookup"><span data-stu-id="667c4-182">Remarks</span></span>

<span data-ttu-id="667c4-183">Si se llama a este método en un almacén de tarjetas inteligentes, se pueden invocar interfaces de usuario de tarjeta inteligente adicionales.</span><span class="sxs-lookup"><span data-stu-id="667c4-183">If this method is called on a SmartCard store, additional SmartCard user interfaces may be invoked.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="667c4-184">Cuando se llama a este método desde un script Web, el script debe tener acceso a los certificados digitales en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="667c4-184">When this method is called from a web script, the script needs to access digital certificates on the local computer.</span></span> <span data-ttu-id="667c4-185">Si permite que el script tenga acceso a los certificados digitales, el sitio web desde el que se ejecuta el script también obtendrá acceso a cualquier información personal almacenada en los certificados.</span><span class="sxs-lookup"><span data-stu-id="667c4-185">If you allow the script to access your digital certificates, the website from which the script is run will also gain access to any personal information stored in the certificates.</span></span> <span data-ttu-id="667c4-186">La primera vez que se llama a este método desde un dominio determinado, se genera un cuadro de diálogo en el que el usuario debe indicar si se debe permitir el acceso a los certificados.</span><span class="sxs-lookup"><span data-stu-id="667c4-186">The first time this method is called from a particular domain, a dialog box is generated in which the user must indicate whether access to the certificates should be allowed.</span></span> <span data-ttu-id="667c4-187">Los almacenes abiertos desde un script web obligan automáticamente a la \_ \_ marca CAPICOM Open \_ exist \_ only.</span><span class="sxs-lookup"><span data-stu-id="667c4-187">Stores opened from a web script automatically force the CAPICOM\_STORE\_OPEN\_EXISTING\_ONLY flag.</span></span>

 

<span data-ttu-id="667c4-188">Si *StoreLocation* es **el \_ \_ almacén de \_ usuarios \_ de tarjetas inteligentes CAPICOM**, *StoreName* se omite.</span><span class="sxs-lookup"><span data-stu-id="667c4-188">If *StoreLocation* is **CAPICOM\_SMART\_CARD\_USER\_STORE**, *StoreName* is ignored.</span></span> <span data-ttu-id="667c4-189">En este caso, CAPICOM Lee todos los certificados de todos los lectores disponibles que contienen una tarjeta inteligente.</span><span class="sxs-lookup"><span data-stu-id="667c4-189">In this case, CAPICOM reads all certificates from all available readers that contain a smart card.</span></span>

## <a name="requirements"></a><span data-ttu-id="667c4-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="667c4-190">Requirements</span></span>



| <span data-ttu-id="667c4-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="667c4-191">Requirement</span></span> | <span data-ttu-id="667c4-192">Value</span><span class="sxs-lookup"><span data-stu-id="667c4-192">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="667c4-193">Redistribuible</span><span class="sxs-lookup"><span data-stu-id="667c4-193">Redistributable</span></span><br/> | <span data-ttu-id="667c4-194">CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP</span><span class="sxs-lookup"><span data-stu-id="667c4-194">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="667c4-195">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="667c4-195">DLL</span></span><br/>             | <dl> <span data-ttu-id="667c4-196"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="667c4-196"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="667c4-197">Vea también</span><span class="sxs-lookup"><span data-stu-id="667c4-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="667c4-198">**Store**</span><span class="sxs-lookup"><span data-stu-id="667c4-198">**Store**</span></span>](store.md)
</dt> <dt>

[<span data-ttu-id="667c4-199">**Objetos de criptografía**</span><span class="sxs-lookup"><span data-stu-id="667c4-199">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="667c4-200">**Cercanos**</span><span class="sxs-lookup"><span data-stu-id="667c4-200">**Close**</span></span>](store-close.md)
</dt> </dl>

 

 
