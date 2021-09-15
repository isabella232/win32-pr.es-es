---
description: Descifra el contenido en sobre.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: Método EnvelopedData.Decrypt
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnvelopedData.Decrypt
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0c4c71ba0e3e0c2d421ad7bcbc9b1a61bb71d284
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476413"
---
# <a name="envelopeddatadecrypt-method"></a>Método EnvelopedData.Decrypt

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use [**la clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System.Security.Cryptography.Pkcs.**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]

El **método Decrypt** descifra el contenido envoltorio. El descifrado se realiza si el destinatario [](../secgloss/p-gly.md) del mensaje tiene acceso [](../secgloss/p-gly.md) a la clave privada emparejada con una de las claves públicas usadas para envolver el mensaje. Al llamar **al método Decrypt** se restablece [*el*](../secgloss/s-gly.md) estado del objeto . Si el **método Decrypt** se realiza correctamente, la [**propiedad Content**](envelopeddata-content.md) del objeto [**EnvelopedData**](envelopeddata.md) se establece en el mensaje de texto no cifrado.

## <a name="syntax"></a>Sintaxis


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EnvelopedMessage* \[ En\]
</dt> <dd>

Cadena que contiene los datos sobres que se descifrarán.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los datos descifrados se convierten [**en el valor de**](envelopeddata-content.md) la propiedad Content para el objeto [**EnvelopedData.**](envelopeddata.md)

Si el usuario de este método no tiene acceso a una clave privada que coincida con una de las claves públicas usadas para envolver el mensaje, se produce un error en el método. Este método producirá un error si el certificado de la clave privada asociada no está en el equipo local Mi almacén o en el almacén MY del usuario actual.

> [!IMPORTANT]
> Cuando se llama a este método desde un script web, el script debe usar la [*clave privada para*](../secgloss/p-gly.md) descifrar los datos. Permitir que los sitios web que no son de confianza usen su clave privada es un riesgo para la seguridad. Aparece un cuadro de diálogo que pregunta si el sitio web puede usar la clave privada cuando se llama por primera vez a este método. Si permite que el script use la clave privada y selecciona "No preguntarme esto de nuevo", el cuadro de diálogo ya no aparecerá para ningún script que use la clave privada para descifrar los datos dentro de ese dominio. Sin embargo, los scripts fuera de ese dominio que intenten usar la clave privada para descifrar los datos seguirán haciendo que aparezca este cuadro de diálogo. Si no permite que el script use la clave privada y selecciona "No preguntarme esto de nuevo", los scripts de ese dominio se rechazarán automáticamente la capacidad de usar la clave privada para descifrar los datos.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2.0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos criptografía**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
