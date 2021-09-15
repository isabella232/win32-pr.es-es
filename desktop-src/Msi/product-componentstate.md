---
description: La propiedad ComponentState es el estado de instalación del componente para la instancia de este producto. Esta propiedad llama a MsiQueryComponentState, con ProductCode, UserSid y Context del objeto .
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Método Product.ComponentState
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473942"
---
# <a name="productcomponentstate-method"></a>Método Product.ComponentState

La **propiedad ComponentState** es el estado de instalación del componente para la instancia de este producto.

Esta propiedad llama [**a MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), con ProductCode, UserSid y Context del objeto . El GUID del identificador de componente se proporciona como parámetro.

## <a name="syntax"></a>Sintaxis


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ID* 
</dt> <dd>

GUID de código de componente del componente, tal como se encuentra en la columna ComponentID de la [tabla Component](component-table.md).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Si la llamada se realiza correctamente, la propiedad contiene el valor como **DWORD**.



| State                | Significado                                            |
|----------------------|----------------------------------------------------|
| INSTALLSTATE \_ LOCAL  | El componente se instala localmente.                |
| INSTALLSTATE \_ SOURCE | El componente se instala para ejecutarse desde el origen. |



 

Si se produce un error en la llamada, la propiedad contiene un código de error de [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).



| Error                     | Significado                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| ERROR \_ DE ACCESO \_ DENEGADO     | El proceso de llamada debe tener privilegios administrativos para obtener información de un usuario distinto del usuario actual. |
| ERROR \_ DE CONFIGURACIÓN NO \_ ACTIVA | Los datos de configuración están dañados.                                                                                 |
| ERROR \_ PARÁMETRO NO \_ VÁLIDO | Se pasó un parámetro no válido a la función .                                                                   |
| ERROR \_ CORRECTO            | La función se completó correctamente.                                                                               |
| COMPONENTE DESCONOCIDO \_ DE \_ ERROR | El identificador de componente no identifica un componente conocido.                                                              |
| ERROR \_ PRODUCTO \_ DESCONOCIDO   | El código de producto no identifica un producto conocido.                                                                |
| ERROR \_ EN LA FUNCIÓN \_   | Error interno inesperado.                                                                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct se define como \_ 000C10A0-0000-0000-C000-00000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Producto**](product-object.md)
</dt> <dt>

[**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[No se admite en Windows Installer 2.0 y versiones anteriores](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




