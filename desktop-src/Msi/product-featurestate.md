---
description: La propiedad FeatureState es el estado de instalación de la característica para la instancia de este producto. Esta propiedad llama a MsiQueryFeatureStateEx, con el ProductCode, UserSid y el contexto del objeto. El identificador de la característica se proporciona como un parámetro.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Product. FeatureState (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f7e602ce5d5b0a8e524f76144c7f1eff8876bb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653537"
---
# <a name="productfeaturestate-method"></a>Product. FeatureState (método)

La propiedad **FeatureState** es el estado de instalación de la característica para la instancia de este producto.

Esta propiedad llama a [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), con el *ProductCode*, *UserSid* y el *contexto* del objeto. El identificador de la característica se proporciona como un parámetro.

## <a name="syntax"></a>Sintaxis


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*FeatureId* 
</dt> <dd>

Identificador de característica que aparece en la columna característica de la [tabla de características](feature-table.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la llamada se realiza correctamente, la propiedad contiene el valor como **DWORD**.



| State                    | Significado                                      |
|--------------------------|----------------------------------------------|
| INSTALLSTATE \_ anunciado | Esta característica se anuncia.                  |
| INSTALLSTATE \_ local      | La característica se instala localmente.            |
| origen de INSTALLSTATE \_     | La característica se instala para ejecutarse desde el origen. |



 

Si se produce un error en la llamada, la propiedad contiene un código de error de [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).



| Error                     | Significado                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ERROR de \_ acceso \_ denegado     | El proceso de llamada debe tener privilegios administrativos para obtener información de un producto instalado para un usuario que no sea el usuario actual. |
| ERROR \_ de \_ Configuración incorrecta | Los datos de configuración están dañados.                                                                                                         |
| ERROR \_ de \_ parámetro no válido | Se pasó un parámetro no válido a la función.                                                                                           |
| ERROR \_ correcto            | La función se completó correctamente.                                                                                                       |
| ERROR \_ de \_ característica desconocida   | El identificador de la característica no identifica una característica conocida.                                                                                          |
| ERROR \_ desconocido del \_ producto   | El código de producto no identifica un producto conocido.                                                                                        |
| ERROR en la \_ función error \_   | Error interno inesperado.                                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer 3,0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct se define como 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Manuales**](product-object.md)
</dt> <dt>

[**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




