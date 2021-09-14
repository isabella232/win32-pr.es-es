---
description: Descomprime el archivo de dispositivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del método Uncompress. Este método se hereda de CIM \_ LogicalFile.
ms.assetid: dfa53b75-56ef-4119-83b9-08b4371762c6
ms.tgt_platform: multiple
title: Método UncompressEx de la CIM_DeviceFile clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceFile.UncompressEx
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a760c31a2067c294ffb43064402ac179c5fba7c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126970268"
---
# <a name="uncompressex-method-of-the-cim_devicefile-class"></a>Método UncompressEx de la clase \_ DeviceFile cim

El **método UncompressEx** descomprime el archivo de dispositivo lógico (o directorio) especificado en la ruta de acceso del objeto. Este método es una versión extendida del [**método Uncompress.**](uncompress-method-in-class-cim-devicefile.md) Este método se hereda de [**CIM \_ LogicalFile**](cim-logicalfile.md).

> [!IMPORTANT]
> Las clases CIM (Modelo de información común) DMTF (Distributed Management Task Force) son las clases primarias en las que se han creado las clases WMI. WMI admite actualmente solo los esquemas [de versión CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

En este tema se usa Managed Object Format sintaxis MOF . Para obtener más información sobre el uso de este método, vea [Llamar a un método](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintaxis


```mof
uint32 UncompressEx(
  [out] string REF StopFileName,
  [in]  string     StartFileName,
  [in]  boolean    Recursive
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*StopFileName* \[ out\]
</dt> <dd>

Cadena que representa el nombre del archivo (o directorio) en el que se ha fallado el método. Este parámetro es **NULL** si el método se realiza correctamente.

</dd> <dt>

*StartFileName* \[ En\]
</dt> <dd>

Cadena que representa el archivo secundario (o directorio) que se usará como punto de partida para el método . Normalmente, el *parámetro StartFileName* es el *parámetro StopFileName* que especifica el archivo o directorio en el que se produjo un error de la llamada al método anterior. Si este parámetro es **NULL,** la operación se realiza en el archivo o directorio especificado en la [**llamada a ExecMethod.**](/windows/desktop/WmiSdk/swbemservices-execmethod)

</dd> <dt>

*Recursivo* \[ En\]
</dt> <dd>

Si **es TRUE,** este método también se aplica de forma recursiva a los archivos y directorios dentro del directorio especificado por la instancia [**de \_ DeviceFile de CIM.**](cim-devicefile.md) En el caso de las instancias de archivo, este parámetro se omite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor de 0 si se ejecuta correctamente y cualquier otro número para indicar un error.

<dl> <dt>


</dt> <dd>

0

Correcto.

</dd> <dt>


</dt> <dd>

2

Acceso denegado.

</dd> <dt>


</dt> <dd>

8

Error no especificado.

</dd> <dt>


</dt> <dd>

9

Objeto no válido.

</dd> <dt>


</dt> <dd>

10

El objeto ya existe.

</dd> <dt>


</dt> <dd>

11

El sistema de archivos no es NTFS.

</dd> <dt>


</dt> <dd>

12

Plataforma no Windows.

</dd> <dt>


</dt> <dd>

13

La unidad no es la misma.

</dd> <dt>


</dt> <dd>

14

El directorio no está vacío.

</dd> <dt>


</dt> <dd>

15

Infracción de uso compartido.

</dd> <dt>


</dt> <dd>

16

Archivo de inicio no válido.

</dd> <dt>


</dt> <dd>

17

Privilegios no mantenidos.

</dd> <dt>


</dt> <dd>

21

Parámetro no válido.

</dd> </dl>

## <a name="remarks"></a>Observaciones

Wmi no implementa actualmente este método. Para usar este método, debe implementarlo en su propio proveedor.

Esta documentación se deriva de las descripciones de clases CIM publicadas por dmtf. Microsoft puede haber realizado cambios para corregir errores menores, ajustarse a los estándares de documentación del SDK de Microsoft o proporcionar más información.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[CIM \_ DeviceFile](uncompressex-method-in-class-cim-devicefile.md)
</dt> <dt>

[**CIM \_ DeviceFile**](cim-devicefile.md)
</dt> </dl>

 

