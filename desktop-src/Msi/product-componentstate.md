---
description: La propiedad ComponentState es el estado de instalación del componente para la instancia de este producto. Esta propiedad llama a MsiQueryComponentState, con ProductCode, UserSid y el contexto del objeto.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Product. ComponentState (método)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 240a854a899f46bf80703bbd6cfb6b1529848586
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653789"
---
# <a name="productcomponentstate-method"></a>Product. ComponentState (método)

La propiedad **ComponentState** es el estado de instalación del componente para la instancia de este producto.

Esta propiedad llama a [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), con ProductCode, UserSid y el contexto del objeto. El GUID del identificador de componente se proporciona como un parámetro.

## <a name="syntax"></a>Sintaxis


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Id* 
</dt> <dd>

GUID del código de componente del componente tal y como se encuentra en la columna ComponentID de la [tabla de componentes](component-table.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la llamada se realiza correctamente, la propiedad contiene el valor como **DWORD**.



| State                | Significado                                            |
|----------------------|----------------------------------------------------|
| INSTALLSTATE \_ local  | El componente se instala localmente.                |
| origen de INSTALLSTATE \_ | El componente se instala para ejecutarse desde el origen. |



 

Si se produce un error en la llamada, la propiedad contiene un código de error de [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).



| Error                     | Significado                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| ERROR de \_ acceso \_ denegado     | El proceso de llamada debe tener privilegios administrativos para obtener información de un usuario que no sea el usuario actual. |
| ERROR \_ de \_ Configuración incorrecta | Los datos de configuración están dañados.                                                                                 |
| ERROR \_ de \_ parámetro no válido | Se pasó un parámetro no válido a la función.                                                                   |
| ERROR \_ correcto            | La función se completó correctamente.                                                                               |
| ERROR \_ de \_ componente desconocido | El identificador de componente no identifica un componente conocido.                                                              |
| ERROR \_ desconocido del \_ producto   | El código de producto no identifica un producto conocido.                                                                |
| ERROR en la \_ función error \_   | Error interno inesperado.                                                                                    |



 

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

[**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[No se admite en Windows Installer 2,0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




