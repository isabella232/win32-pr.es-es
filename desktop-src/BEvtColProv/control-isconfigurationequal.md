---
description: Compare el argumento con la configuración activa del recopilador.
ms.assetid: 8decb674-c905-4eb6-9f78-7bc7b99db908
ms.tgt_platform: multiple
title: Método IsConfigurationEqual de la clase control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.IsConfigurationEqual
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: fb471f144a39519f1f724db458b57b624db2846d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103806991"
---
# <a name="isconfigurationequal-method-of-the-control-class"></a>Método IsConfigurationEqual de la clase control

Compare el argumento con la configuración activa del recopilador.

## <a name="syntax"></a>Sintaxis


```mof
Uint32 IsConfigurationEqual(
  [in] string Config
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Configuración* \[ de de\]
</dt> <dd>

Configuración que se va a comparar con la configuración activa.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

<dl> <dt>


</dt> <dd>

0

Error

</dd> <dt>


</dt> <dd>

1

Correcto

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10 \[\]<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2016<br/>                                                                       |
| Espacio de nombres<br/>                | Raíz de \\ Microsoft \\ Windows \\ BootEventCollector<br/>                                              |
| MOF<br/>                      | <dl> <dt>BootEventCollectorWMI. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>BEvtCol.exe</dt> </dl>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control**](control.md)
</dt> </dl>

 

 




