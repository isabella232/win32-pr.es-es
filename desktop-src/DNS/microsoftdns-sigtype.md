---
title: MicrosoftDNS_SIGType clase
description: Subclase de ResourceRecord de MicrosoftDNS que representa un registro de recursos de firma \_ (SIG).
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- MicrosoftDNS_SIGType dns de clase
- MicrosoftDNS_SIGType clase DNS , descrita
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
- MicrosoftDNS_SIGType.Modify
- MicrosoftDNS_SIGType.TypeCovered
- MicrosoftDNS_SIGType.Algorithm
- MicrosoftDNS_SIGType.Labels
- MicrosoftDNS_SIGType.OriginalTTL
- MicrosoftDNS_SIGType.SignatureExpiration
- MicrosoftDNS_SIGType.SignatureInception
- MicrosoftDNS_SIGType.KeyTag
- MicrosoftDNS_SIGType.SignerName
- MicrosoftDNS_SIGType.Signature
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17009bf6458bd51b1d7a41b31f33ad0695e0da1a41c77aa72f56ee01573a529
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118163176"
---
# <a name="microsoftdns_sigtype-class"></a>Clase SIGType de MicrosoftDNS \_

Subclase de [**\_ ResourceRecord de MicrosoftDNS**](microsoftdns-resourcerecord.md) que representa un registro de recursos de firma (SIG).

La sintaxis siguiente se simplifica a partir del código MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
class MicrosoftDNS_SIGType : MicrosoftDNS_ResourceRecord
{
  uint16 TypeCovered;
  uint16 Algorithm;
  uint16 Labels;
  uint32 OriginalTTL;
  uint32 SignatureExpiration;
  uint32 SignatureInception;
  uint16 KeyTag;
  string SignerName;
  string Signature;
};
```

## <a name="members"></a>Miembros

La **clase \_ SIGType de MicrosoftDNS** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La **clase \_ SIGType de MicrosoftDNS** tiene estos métodos.



| Método                             | Descripción                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | Crea instancias de un RR de SIG en función de los datos de los parámetros de entrada del método: el nombre del servidor DNS del registro, el nombre del contenedor, el nombre de propietario, la clase (valor predeterminado = IN), el valor de período de vida y la marca de asignación WINS, el tiempo de espera de búsqueda inversa, el tiempo de espera de caché WINS y el nombre de dominio que se va a anexar. Devuelve una referencia al nuevo objeto como parámetro de salida. <br/> Calificadores: implementados, estáticos<br/>                                                                                                                                                                                                                                                       |
| **Modificar**                         | Actualiza el TTL, la marca de asignación, el tiempo de espera de búsqueda, el tiempo de espera de caché y el dominio de resultados a los valores especificados como parámetros de entrada de este método. Si no se especifica un nuevo valor para un parámetro, no se cambia el valor actual del parámetro. El método devuelve una referencia al objeto modificado como parámetro de salida. <br/> Calificadores: Implementado<br/> **Windows Server 2003:** Este método también actualiza TypeCovered, Algorithm, Labels, OriginalTTL, SignatureExpiration, SignatureInception, KeyTag, SignerName y Signature a los valores especificados como parámetros de entrada de este método.<br/> <br/> |



 

### <a name="properties"></a>Propiedades

La **clase \_ SIGType de MicrosoftDNS** tiene estas propiedades.

<dl> <dt>

**Algoritmo**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Algoritmo utilizado con la clave especificada en el registro de recursos. Los valores asignados se muestran en la tabla siguiente.



| Valor                                                                                                | Significado                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537)<br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539)<br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536)<br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | Criptografía de curva elíptica<br/> |



 

</dd> <dt>

**KeyTag**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Método utilizado para elegir una clave que comprueba una SIG. Consulte RFC 2535, Apéndice C para ver el método usado para calcular un KeyTag.

</dd> <dt>

**Etiquetas**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Recuento sin signo de etiquetas en el nombre original del propietario rr. de SIG. El recuento no incluye la etiqueta NULL para la raíz ni ningún carácter comodín inicial.

</dd> <dt>

**OriginalTTL**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

TTL del conjunto rr firmado por sig.

</dd> <dt>

**Signature**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Firma, representada en base 64, con el formato definido en RFC 2535, Apéndice A.

</dd> <dt>

**SignatureExpiration**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha de expiración de la firma, expresada en segundos desde el principio del 1 de enero de 1970, hora media de Greenwich (GMT), excepto los segundos bisiestos.

</dd> <dt>

**SignatureInception**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Fecha y hora en que la firma se convierte en válida, expresada en segundos desde el principio del 1 de enero de 1970, hora media de Greenwich (GMT), excepto los segundos bisiestos.

</dd> <dt>

**SignerName**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Nombre de dominio del firmante que generó el RR de SIG.

</dd> <dt>

**TypeCovered**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint16**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Tipo de RR cubierto por esta SIG.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                   |
| Espacio de nombres<br/>                | \\MicrosoftDNS raíz<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov.mof</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Método CreateInstanceFromPropertyData de la clase SIGType de MicrosoftDNS \_**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Método Modify de la clase SIGType de MicrosoftDNS \_**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**ResourceRecord de MicrosoftDNS \_**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





