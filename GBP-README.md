# Global Business Performance

## Sumário

* [Origem da Tabela principal](#origem-da-tabela-principal)
    * [Mapeamento dos campos da Tabela Principal](#mapeamento-dos-campos-da-tabela-principal)
* [Criação da Tabela inicial](#criação-da-tabela-intermediária)
* [Base de cálculo das colunas da tabela mencionada](#base-de-cálculo-das-colunas-da-tabela-mencionada)
    * [1 shipment_tons](#1-shipment_tons)
    * [2 net_sales](#2-net_sales)
        * [2.1 gross_sales_usd](#21-gross_sales_usd)
        * [2.2 cash_discounts_usd](#22-cash_discounts_usd)
        * [2.3 rebate_usd](#23-rebate_usd)
        * [2.4 sales_discounts_usd](#24-sales_discounts_usd)
        * [2.5 pis_tax_usd](#25-pis_tax_usd)
        * [2.6 ipi_tax_usd](#26-ipi_tax_usd)
        * [2.7 cofins_tax_usd](#27-cofins_tax_usd)
        * [2.8 icms_tax_usd](#28-icms_tax_usd)
        * [2.9 other_taxes_1_usd](#29-other_taxes_1_usd)
        * [2.10 other_taxes_2_usd](#210-other_taxes_2_usd)
        * [2.11 other_taxes_3_usd](#211-other_taxes_3_usd)
    * [3 cost_of_sales](#3-cost_of_sales)
        * [3.1 cost_of_goods](#31-cost_of_goods)
            * [3.1.1 raw_material_usd](#311-raw_material_usd)
            * [3.1.2 reduction_usd](#312-reduction_usd)
            * [3.1.3 variable_cost_usd](#313-variable_cost_usd)
            * [3.1.4 fixed_cost_usd](#314-fixed_cost_usd)
        * [3.2 total_freights](#32-total_freights)
            * [3.2.1 freight_paid_usd](#321-freight_paid_usd)
            * [3.2.2 general_shipping_usd](#322-general_shipping_usd)
            * [3.2.3 plant_shipping_usd](#323-plant_shipping_usd)
            * [3.2.4 port_expenses_usd](#324-port_expenses_usd)
            * [3.2.5 general_frete_outros_usd](#325-general_frete_outros_usd)
            * [3.2.6 plant_frete_outros_usd](#326-plant_frete_outros_usd)
        * [3.3 extraordinário](#33-extraordinário)
            * [3.3.1 plant_extraordinario_usd](#331-plant_extraordinario_usd)
            * [3.3.2 general_extraordinario_usd](#332-general_extraordinario_usd)
        * [3.4 chargeback_precificacao](#34-chargeback_precificacao)
            * [3.4.1 plant_precificacao_usd](#341-plant_precificacao_usd)
            * [3.4.2 general_precificacao_usd](#342-general_precificacao_usd)
        * [3.5 outros_custos](#35-outros_custos)
            * [3.5.1 general_outros_custos_usd](#351-general_outros_custos_usd)
            * [3.5.2 plant_outros_custos_usd](#352-plant_outros_custos_usd)
    * [4 gross_profit](#4-gross_profit)
        * [4.1 net_sales](#41-net_sales)
        * [4.2 cost_of_sales](#42-cost_of_sales)
    * [5 sg_&_a](#5-sg__a)
        * [5.1 general_sales_expenses_usd](#51-general_sales_expenses_usd)
        * [5.2 plant_sales_expenses_usd](#52-plant_sales_expenses_usd)
        * [5.3 general_gen_adm_expenses_usd](#53-general_gen_adm_expenses_usd)
        * [5.4 plant_gen_adm_expenses_usd](#54-plant_gen_adm_expenses_usd)
        * [5.5 general_sgg_it_procur_usd](#55-general_sgg_it_procur_usd)
        * [5.6 plant_sgg_it_procur_usd](#56-plant_sgg_it_procur_usd)
    * [6 impairement_loss](#6-impairement_loss)
        * [6.1 general_pdd_usd](#61-general_pdd_usd)
        * [6.2 plant_pdd_usd](#62-plant_pdd_usd)
    * [7 other_income_&_expenses](#7-other_income__expenses)
        * [7.1 plant_other_income_expenses_usd](#71-plant_other_income_expenses_usd)
        * [7.2 general_other_income_expenses_usd](#72-general_other_income_expenses_usd)
    * [8 depreciation](#8-depreciation)
        * [8.1 plant_depreciation_amortization_usd](#81-plant_depreciation_amortization_usd)
        * [8.2 general_depreciation_amortization_usd](#82-general_depreciation_amortization_usd)
    

## Origem da Tabela principal

* catalogo: corporate_trusted_prd
* Schema: global_sapecc_financial
* Tabela: tb_ce1gopc

### Mapeamento dos campos da Tabela Principal

#### Informações de Atributos

* mtart - nome de referência -> Tipo Material
* kndnr - nome de referência -> Número do cliente
* rec_waers - nome de referência -> moeda
* bktxt - nome de referência -> Texto explicativo

#### Informações numéricas

* vv001 - nome de referência -> Total Shipment (tons)
* vv010 - nome de referência -> Gross Sales (basic)
* vv011 - nome de referência -> Inland Freight
* vv012 - nome de referência -> Port Expenses
* vv013 - nome de referência -> Coal Cost (variable)
* vv015 - nome de referência -> Inland Freight 
* vv016 - nome de referência -> Coke Cost (variable)
* vv018 - nome de referência -> Scrap Cost (variable)
* vv019 - nome de referência -> Pig Iron Cost (variable)
* vv020 - nome de referência -> Alloys Cost (variable)
* vv021 - nome de referência -> Other Materials Cost
* vv022 - nome de referência -> Fuel Pre-reheat (fixed)
* vv023 - nome de referência -> Electricity (fixed)
* vv024 - nome de referência -> Oxigen (variable)
* vv025 - nome de referência -> Refractory (fixed)
* vv026 - nome de referência -> Electrodes (fixed)
* vv027 - nome de referência -> Other Specific Material (fixed)
* vv028 - nome de referência -> Personnel (fixed)
* vv029 - nome de referência -> Depreciation
* vv030 - nome de referência -> Maintenance (fixed)
* vv031 - nome de referência -> Other General Expenses (fixed)
* vv038 - nome de referência -> Cash Discounts
* vv041 - nome de referência -> Other taxes 1
* vv042 - nome de referência -> Other taxes 2
* vv043 - nome de referência -> ICMS
* vv044 - nome de referência -> IPI
* vv045 - nome de referência -> PIS
* vv046 - nome de referência -> COFINS
* vv047 - nome de referência -> Other taxes 3
* vv048 - nome de referência -> Rebates
* vv049 - nome de referência -> Rebates
* vv060 - nome de referência -> 
* vv061 - nome de referência -> Freight  Revenue
* vv071 - nome de referência -> Insurance FI
* vv072 - nome de referência -> Electricity (variable)
* vv073 - nome de referência -> Oxigen (variable)
* vv074 - nome de referência -> Refractory (variable)
* vv075 - nome de referência -> Electrodes (variable)
* vv076 - nome de referência -> Other Specific Material (variable)
* vv077 - nome de referência -> Personnel (variable)
* vv078 - nome de referência -> Maintenance (variable)
* vv079 - nome de referência -> Other General Expenses (variable)
* vv080 - nome de referência -> Fuel Pre-reheat (variable)
* vv083 - nome de referência -> Port Expenses
* vv084 - nome de referência -> Insurance SD
* vv085 - nome de referência -> Overseas FreightSD
* vv086 - nome de referência -> FreightFI

Objetivo: É fonte dos dados brutos que contêm todos as informações que serão propagados na tabela 2. abaixo.

## Criação da Tabela inicial

* catalogo: corporate_globalbusinessperformance_refined
* Schema: global_profitability
* Tabela: tb_pa_main_temp

Objetivo: Filtrar os dados necessários para as transformações posteriores que serão refinadas conforme regras de negócio.

## Criação da Tabela intermediária

* catalogo: corporate_globalbusinessperformance_refined
* Schema: global_profitability
* Tabela: tb_pa_detail_temp

Objetivo: Aplicar regras de negócio para refinar os dados.

### Base de cálculo das colunas da tabela mencionada

* Início dos cálculos propóstos neste trabalho.

## Regra de Rateio

Agrupamento tons

$$ tons\ =\ \sum_{}(vv001) $$

Divisão pela coluna mencionada de rateio geral

$$ \frac{tons}{coluna\_de\_rateio\_geral} $$

Agrupamento depreciação

$$ \frac{vv029}{avg\_exchange\_rate} $$

Divisão pela coluna mencionada de rateio depreciação

$$ \frac{tons}{coluna\_de\_rateio\_depreciação} $$

* [Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

## 1 shipment_tons

Quando a coluna << mtart >>  está contida nos materiais:
    
* ('#', 'ZABF', 'ZERP', 'ZIEN', 'ZMET', 'ZROH', 'ZRSA')
    
Retorna

$$ 0 $$
    
Caso contrário retorna

$$ \frac{(vv001)}{1000} $$
    
* [Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

## 2 net_sales

Composição do cálculo

$$ net\_sales = gross\_sales\_usd + cash\_discounts\_usd + rebate\_usd + sales\_discounts\_usd + pis\_tax\_usd + ipi\_tax\_usd + cofins\_tax\_usd + icms\_tax\_usd + other\_taxes\_1\_usd + other\_tax

---

### 2.1 gross_sales_usd
---

Quando a coluna << kndnr >> contém ('0000004773', '0000004775')

Retorna

$$ 0 $$

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ vv010 $$

Caso contrário retorna 

$$ \frac{(vv010)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

### 2.2 cash_discounts_usd
---

Quando a coluna << rec_waers >> é 'USD'

Retorna

$$ vv038\ *\ -1 $$

Caso contrário retorna

$$ \frac{(vv038\ *\ -1)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

### 2.3 rebate_usd
---

Quando o texto da coluna << bktxt >> não for nulo para o campo

Retorna

$$ 0 $$

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ vv048\ -\ vv049 $$

Caso contrário retorna

$$ \frac{(vv048\ -\ vv049)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

### 2.4 sales_discounts_usd
---

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ vv060\ +\ (vv041\ *\ -1) $$

Caso contrário retorna

$$ \frac{vv060\ + (vv041\ *\ -1)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

### 2.5 pis_tax_usd
---

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ vv045 $$

Caso contrário retorna

$$ \frac{(vv045)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

### 2.6 ipi_tax_usd
---

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ vv044 $$

Caso contrário retorna

$$ \frac{(vv044)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

### 2.7 cofins_tax_usd
---

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ vv046 $$

Caso contrário retorna

$$ \frac{(vv046)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

### 2.8 icms_tax_usd
---

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ vv043 $$

Caso contrário retorna

$$ \frac{(vv043)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

### 2.9 other_taxes_1_usd
---

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ vv041 $$

Caso contrário retorna

$$ \frac{(vv041)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

### 2.10 other_taxes_2_usd
---

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ vv042 $$

Caso contrário retorna

$$ \frac{(vv042)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

### 2.11 other_taxes_3_usd
---

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ vv047 $$

Caso contrário retorna

$$ \frac{(vv047)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

## 3 cost_of_sales

É a somatória dos campos conforme a composição abaixo

$$ cost\_of\_sales\ =\ cost\_of\_goods\ +\ total\_freights\ +\ extraordinário\ +\ chargeback\_precificacao\ +\ outros\_custos $$

---

### 3.1 cost_of_goods
---

É a somatória dos campos conforme a composição abaixo
$$ cost\_of\_goods\ =\ raw\_material\_usd\ +\ reduction\_usd\ +\ variable\_cost\_usd\ +\ fixed\_cost\_usd $$

---

#### 3.1.1 raw_material_usd
---

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ (vv018\ *\ -1)\ -\ vv019\ -\ vv020\ -\ vv021 $$

Caso contrário retorna

$$ \frac{(vv018\ *\ -1)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

#### 3.1.2 reduction_usd
---

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ (vv018\ *\ -1)\ -\ vv019\ -\ vv020\ -\ vv021 $$

Caso contrário retorna

$$ \frac{(vv018\ *\ -1)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

#### 3.1.3 variable_cost_usd
---

Quando a coluna << shipment_tons >> for nula

Retorna

$$ resultado\ =\ (vv077\ *\ -1)\ -\ vv072\ -\ vv073\ -\ vv080\ -\ vv075\ -\ vv074\ -\ vv076\ -\ vv078\ -\ vv079 $$

Caso contrário retorna

$$ resultado\ =\ vv001\ *\ \frac{(variable\_cost\_lc\_per\_ship\_ton)}{1000} $$

Após a lógica retona

$$ \frac{(resultado)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

#### 3.1.4 fixed_cost_usd
---

Quando a coluna << shipment_tons >> for nula

Retorna

$$ resultado\ =\ (vv028 * -1)\ -\ vv023\ -\ vv024\ -\ vv022\ - vv025\ -\ vv026\ -\ vv027\ -\ vv030\ -\ vv029\ -\ vv031 $$

Caso contrário retorna

$$ resultado\ =\ vv001\ *\ \frac{(fixed\_cost\_lc\_per\_ship\_ton)}{1000} $$

Após a lógica retona

$$ \frac{(resultado)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

### 3.2 total_freights
---

É a somatória conforme a composição abaixo

$$ total\_freights\ =\ freight\_paid\_usd\ +\ general\_shipping\_usd\ +\ plant\_shipping\_usd\ +\ port\_expenses\_usd\ +\ general\_frete\_outros\_usd\ +\ plant\_frete\_outros\_usd $$

---

#### 3.2.1 freight_paid_usd
---

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ (vv011\ -\ vv015)\ +\ (vv085\ -\ vv086)\ +\ (vv084\ -\ vv071) $$

Caso contrário retorna

$$ \frac{(vv011\ -\ vv015)\ +\ (vv085\ -\ vv086)\ +\ (vv084\ -\ vv071)}{avg\_exchange\_rate} $$

[Nomenclatura de Campos](#mapeamento-dos-campos-da-tabela-principal)

---

#### 3.2.2 general_shipping_usd
---

Cálculo general_shipping

$$ general\_shipping = \frac{(general\_shipping\_amt)}{tons} $$

Quando a combinação das colunas:

* << sales_type >> for 'Product_Sales'
* << external_internal >> for 'External'

Retorna

$$ shipment\_tons\ *\ general\_shipping $$

Caso contrário retorna

$$ 0 $$

origens

* tb_final_with_texts_temp
* allocations_plant_alloc

---

#### 3.2.3 plant_shipping_usd
---

Quando a combinação das colunas:

* << plant >> começa com 6
* << sales_type >> for 'Other'
* << external_internal >> for 'External'
    
Retorna

$$ shipment\_tons\ *\ plant\_shipping $$

Quando a combinação das colunas:

* << plant >> começa com 6
* << sales_type >> for 'Product_Sales'
* << external_internal >> for 'External'

Retorna

$$ shipment\_tons\ *\ plant\_shipping $$

Caso contrário retorna

$$ 0 $$

---

#### 3.2.4 port_expenses_usd
---

Quando a coluna << rec_waers >> for 'USD'

Retorna

$$ vv012\ -\ vv083 $$

Caso contrário retorna

$$ \frac{(vv012\ -\ vv083)}{avg\_exchange\_rate} $$

---

#### 3.2.5 general_frete_outros_usd
---

Quando a combinação das colunas:

* << sales_type >> for 'Product_Sales'
* << external_internal >> for 'External'

$$ shipment\_tons\ *\ general\_frete\_outros $$

Caso contrário retorna

$$ 0 $$

coalesce(CASE 
        WHEN a.sales_type = 'Product_Sales' 
        AND a.external_internal = 'External'
        THEN a.shipment_tons * b.general_frete_outros
        ELSE 0
    END, 0)           general_frete_outros_usd,

---

#### 3.2.6 plant_frete_outros_usd
---

Quando a combinação das colunas:

* << plant >> começa com 6
* << sales_type >> for 'Other'
* << external_internal >> for 'External'

Retorna

$$ shipment\_tons\ *\ plant\_frete\_outros $$

Quando a combinação das colunas:

* << plant >> começa com 6
* << sales_type >> for 'Product_Sales'
* << external_internal >> for 'External'

Retorna

$$ shipment\_tons\ *\ plant\_frete_outros $$

Caso contrário retorna

$$ 0 $$

---

### 3.3 extraordinário
---
É a somatória dos campos conforme a composição abaixo

$$ plant\_extraordinario\_usd\ +\ general\_extraordinario\_usd $$

---

#### 3.3.1 plant_extraordinario_usd
---

Quando a combinação das colunas:

* << plant >> começa com 6
* << sales_type >> for 'Other'
* << external_internal >> for 'External'

Retorna

$$ shipment\_tons\ *\ plant\_extraordinario $$

Quando a combinação das colunas:

* << plant >> começa com 6
* << sales_type >> for 'Product_Sales'
* << external_internal >> for 'External'

Retorna

$$ shipment\_tons\ *\ plant\_extraordinario $$

Caso contrário retorna

$$ 0 $$

---

#### 3.3.2 general_extraordinario_usd
---

Agrupamento

$$ tons\ =\ \sum_{}(shipment\_tons) $$

Divisão

$$ general\_extraordinario = \frac{general\_extraordinario\_amt}{tons} $$

Quando a combinação das colunas:

* << sales_type >> for 'Product_Sales'
* << external_internal >> for 'External'

Retorna

$$ shipment\_tons\ *\ general\_extraordinario $$

Caso contrário retorna

$$ 0 $$

origens

* tb_final_with_texts_temp
* tb_sales_tons_temp

---

#### 3.4 chargeback_precificacao
---
É a somatória dos campos conforme a composição abaixo

$$ plant\_precificacao\_usd\ +\ general\_precificacao\_usd $$

---

#### 3.4.1 plant_precificacao_usd
---
Ajustar aqui!

---

#### 3.4.2 general_precificacao_usd
---
Ajustar aqui!

---

### 3.5 outros_custos
---
É a somatória dos campos conforme a composição abaixo

$$ general\_outros\_custos\_usd\ +\ plant\_outros\_custos\_usd $$

---

#### 3.5.1 general_outros_custos_usd
---
Ajustar aqui!

---

#### 3.5.2 plant_outros_custos_usd
---
Ajustar aqui!

---

## 4 gross_profit

É a somatória dos campos conforme a composição abaixo

$$ net\_sales\ +\ cost\_of\_sales $$

---

### 4.1 net_sales
---
Link da base de cálculo

[2 net_sales](#2-net_sales)

---

### 4.2 cost_of_sales
---
Link da base de cálculo

[3 cost_of_sales](#3-cost_of_sales)

---

## 5 sg_&_a

É a somatória dos campos conforme a composição abaixo

$$ general\_sales\_expenses\_usd\ +\ plant\_sales\_expenses\_usd\ +\ general\_gen\_adm\_expenses\_usd\ +\ plant\_gen\_adm\_expenses\_usd\ +\ general\_sgg\_it\_procur\_usd\ +\ plant\_sgg\_it\_procur\_usd $$

---

### 5.1 general_sales_expenses_usd
---

Quando a combinação das colunas:

* << sales_type >> for 'Product_Sales'
* << external_internal >> for 'External'

Retorna

$$ shipment\_tons\ *\ general\_sales\_expenses $$

Caso contrário retorna

$$ 0 $$

coalesce(CASE 
        WHEN a.sales_type = 'Product_Sales' 
        AND a.external_internal = 'External'
        THEN a.shipment_tons * b.general_sales_expenses
        ELSE 0
    END, 0)           general_sales_expenses_usd,

---

### 5.2 plant_sales_expenses_usd
---
Ajustar aqui!

---

### 5.3 general_gen_adm_expenses_usd
---
Ajustar aqui!

---

### 5.4 plant_gen_adm_expenses_usd
---
Ajustar aqui!

---

### 5.5 general_sgg_it_procur_usd
---
Ajustar aqui!

---

### 5.6 plant_sgg_it_procur_usd
---
Ajustar aqui!

---

## 6 impairement_loss

É a somatória dos campos conforme a composição abaixo

$$ general\_pdd\_usd\ +\ plant\_pdd\_usd $$

---

### 6.1 general_pdd_usd
---
Ajustar aqui!

---

### 6.2 plant_pdd_usd
---
Ajustar aqui!

---

## 7 other_income_&_expenses

É a somatória dos campos conforme a composição abaixo

$$ plant\_other\_income\_expenses\_usd + general\_other\_income\_expenses\_usd $$

### 7.1 plant_other_income_expenses_usd
---
Ajustar aqui!

---

### 7.2 general_other_income_expenses_usd
---
Ajustar aqui!

---

## 8 depreciation

É a somatória dos campos conforme a composição abaixo

$$ plant\_depreciation\_amortization\_usd + general\_depreciation\_amortization\_usd $$

--
### 8.1 plant_depreciation_amortization_usd
---
Ajustar aqui!

---

### 8.2 general_depreciation_amortization_usd
---
Ajustar aqui!

---
