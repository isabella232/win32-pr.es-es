---
description: La propiedad FeatureState es el estado de instalación de la característica para la instancia de este producto. Esta propiedad llama a MsiQueryFeatureStateEx, con ProductCode, UserSid y Context del objeto . El identificador de característica se proporciona como parámetro.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Método Product.FeatureState
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
ms.openlocfilehash: 484b8f7f3094cf5bca2cb9d03941d68619995ba98de08e2845c3717439709e2b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129055"
---
# <a name="productfeaturestate-method"></a>Método Product.FeatureState

La **propiedad FeatureState** es el estado de instalación de la característica para la instancia de este producto.

Esta propiedad llama [**a MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), con *ProductCode*, *UserSid* y *Context* del objeto . El identificador de característica se proporciona como parámetro.

## <a name="syntax"></a>Sintaxis


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Featureid* 
</dt> <dd>

Identificador de característica que aparece en la columna Característica de la [tabla de características](feature-table.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Si la llamada se realiza correctamente, la propiedad contiene el valor como **DWORD**.



| State                    | Significado                                      |
|--------------------------|----------------------------------------------|
| INSTALLSTATE \_ ANUNCIADO | Esta característica se anuncia.                  |
| INSTALLSTATE \_ LOCAL      | La característica se instala localmente.            |
| INSTALLSTATE \_ SOURCE     | La característica se instala para ejecutarse desde el origen. |



 

Si se produce un error en la llamada, la propiedad contiene un código de error de [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).



| Error                     | Significado                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ACCESO DE ERROR \_ \_ DENEGADO     | El proceso de llamada debe tener privilegios administrativos para obtener información de un producto instalado para un usuario distinto del usuario actual. |
| ERROR \_ DE CONFIGURACIÓN NO \_ ACTIVA | Los datos de configuración están dañados.                                                                                                         |
| ERROR \_ PARÁMETRO NO \_ VÁLIDO | Se pasó un parámetro no válido a la función.                                                                                           |
| ERROR \_ CORRECTO            | La función se completó correctamente.                                                                                                       |
| CARACTERÍSTICA DESCONOCIDA \_ DE \_ ERROR   | El identificador de característica no identifica una característica conocida.                                                                                          |
| ERROR \_ PRODUCTO \_ DESCONOCIDO   | El código de producto no identifica un producto conocido.                                                                                        |
| ERROR EN \_ LA FUNCIÓN \_   | Error interno inesperado.                                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct se define como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Producto**](product-object.md)
</dt> <dt>

[**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




