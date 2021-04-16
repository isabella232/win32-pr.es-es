---
description: Descifra el contenido con doble cifrado.
ms.assetid: 717d0595-e8bb-4725-bd53-fc1281cbc8ee
title: EnvelopedData. Decrypt (método)
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
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649801"
---
# <a name="envelopeddatadecrypt-method"></a>EnvelopedData. Decrypt (método)

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la [**clase EnvelopedCms**](/dotnet/api/system.security.cryptography.pkcs.envelopedcms?view=dotnet-plat-ext-3.1&preserve-view=true) en el espacio de nombres [**System. Security. Cryptography. Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) .\]

El método de **descifrado** descifra el contenido con doble cifrado. El descifrado se realiza si el destinatario del mensaje tiene acceso a la [*clave privada*](../secgloss/p-gly.md) emparejada con una de las [*claves públicas*](../secgloss/p-gly.md) que se usan para envolver el mensaje. Al llamar al método **Decrypt** se restablece el [*Estado*](../secgloss/s-gly.md) del objeto. Si el método de **descifrado** se realiza correctamente, la propiedad [**Content**](envelopeddata-content.md) del objeto [**EnvelopedData**](envelopeddata.md) se establece en el mensaje de texto simple.

## <a name="syntax"></a>Sintaxis


```VB
EnvelopedData.Decrypt( _
  ByVal EnvelopedMessage _
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*EnvelopedMessage* \[ de\]
</dt> <dd>

Cadena que contiene los datos con doble cifrado que se van a descifrar.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Los datos descifrados se convierten en el valor de la propiedad de [**contenido**](envelopeddata-content.md) para el objeto [**EnvelopedData**](envelopeddata.md) .

Si el usuario de este método no tiene acceso a una clave privada que coincida con una de las claves públicas que se usan para envolver el mensaje, se produce un error en el método. Este método producirá un error si el certificado de la clave privada asociada no está en el almacén del equipo local o en el usuario actual.

> [!IMPORTANT]
> Cuando se llama a este método desde un script Web, el script debe usar la [*clave privada*](../secgloss/p-gly.md) para descifrar los datos. Permitir a los sitios web que no son de confianza usar su clave privada es un riesgo para la seguridad. Un cuadro de diálogo que pregunta si el sitio web puede usar su clave privada aparece cuando se llama por primera vez a este método. Si permite que el script use su clave privada y selecciona "no volver a preguntar", el cuadro de diálogo ya no aparecerá en ningún script que use la clave privada para descifrar los datos dentro de ese dominio. Sin embargo, los scripts fuera de ese dominio que intenten usar su clave privada para descifrar los datos seguirán generando este cuadro de diálogo. Si no permite que el script use su clave privada y selecciona "no volver a preguntar", se rechazará automáticamente la capacidad de usar la clave privada para descifrar los datos de los scripts dentro de ese dominio.

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fin de compatibilidad de cliente<br/> | Windows Vista<br/>                                                               |
| Fin de compatibilidad de servidor<br/> | Windows Server 2008<br/>                                                         |
| Redistribuible<br/>       | CAPICOM 2,0 o posterior en Windows Server 2003 y Windows XP<br/>                  |
| Archivo DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Objetos de criptografía**](cryptography-objects.md)
</dt> <dt>

[**EnvelopedData**](envelopeddata.md)
</dt> </dl>

 

 
